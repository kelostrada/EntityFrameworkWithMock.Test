EntityFrameworkWithMock.Test
============================

Entity Framework using mocking with Moq

I had a problem with creating mocks when I used methods like `ToList` on the DbSets directly.
The enumerator was being kept in the same state on every set so you couldn't call such methods there. 
The solution for that was pretty simple - you had to pass the enumerator not directly, but as a function
which would create new enumerator (resetted one) every time you would call your DbSet.
