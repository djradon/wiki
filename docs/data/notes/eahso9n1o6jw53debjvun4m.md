
## Code Organization

### By Module/Folder

```
Features/
├── Users/
│   ├── GetUsers/
│   ├── CreateUser/
│   ├── SetUserActive/
│   └── ...
├── Orders/
│   ├── PlaceOrder/
│   ├── CancelOrder/
│   └── ...
```

### Onion by Module/Folder

```
MyApplication.sln
│
├── Modules/
│   ├── UsersModule/
│   │   ├── UsersModule.csproj
│   │   ├── Domain/
│   │   │   └── ...
│   │   ├── Application/
│   │   │   ├── Services/
│   │   │   ├── DTOs/
│   │   │   └── ...
│   │   └── Infrastructure/
│   │       ├── Repositories/
│   │       └── ...
│   │
│   ├── OrdersModule/
│   │   ├── OrdersModule.csproj
│   │   ├── Domain/
│   │   │   └── ...
│   │   ├── Application/
│   │   │   ├── Services/
│   │   │   ├── DTOs/
│   │   │   └── ...
│   │   └── Infrastructure/
│   │       ├── Repositories/
│   │       └── ...
│   │
│   └── ...
│
└── WebApp/
    ├── WebApp.csproj
    ├── Pages/
    ├── Program.cs
    └── ...
```

## References

- https://levelup.gitconnected.com/the-core-question-are-vertical-slices-just-modular-monoliths-9b1ef2358c53