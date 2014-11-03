EntityFrameworkWithMock.Test
============================

Entity Framework using mocking with Moq

I had a problem with creating mocks when I used methods like `ToList` on the DbSets directly.
The enumerator was being kept in the same state on every set so you couldn't call such methods there. 
The solution for that was pretty simple - you had to pass the enumerator not directly, but as a function
which would create new enumerator (resetted one) every time you would call your DbSet.

The project is based on the tutorial I took from MSDN for creating mocks with Entity Framework: http://msdn.microsoft.com/en-us/data/dn314429.aspx#async

The code they provided wasn't acting as expected so I needed to figure the solution. Please create pull requests if you think something should be added here or something could be corrected.
