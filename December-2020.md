# 12/22

EFCore 5 can log via the DbContextOptionsBuilders via:

```csharp
LogTo()
```

Another can be used to include application data in messages via the options builder object as well:

```csharp
EnableSensitiveDataLogging()
```

EFCore 5 can auto delete the whole database via:

```csharp
Database.EnsureDeleted();
```

EFCore 5 can filter includes:

```csharp
planes.Include(x => x.AircraftType.Where(y => y.Id == id));
```
