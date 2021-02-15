# Autofac.Extras.NHibernate

[Autofac](https://autofac.org) implementation of the NHibernate factories that allow for dependency injection into entities and NHibernate objects.

[![Build status](https://ci.appveyor.com/api/projects/status/vpkf5dlbw5ehfeng?svg=true)](https://ci.appveyor.com/project/Autofac/autofac-extras-nhibernate)

> :warning: **MAINTENANCE MODE**: This package is in maintenance-only mode. Bug fixes may be addressed and Autofac compatibility may be checked but no new features will be added.

Please file issues and pull requests for this package in this repository rather than in the Autofac core repo.

- [NuGet](https://www.nuget.org/packages/Autofac.Extras.NHibernate/)
- [Contributing](https://autofac.readthedocs.io/en/latest/contributors.html)

## Usage

The provider is [based on the blog article here](https://www.chadly.net/dependency-injection-with-nhibernate-and-autofac/).

```csharp
var builder = new ContainerBuilder();
var container = builder.Build();

Environment.BytecodeProvider = new AutofacBytecodeProvider(
    container,
    new ProxyFactoryFactory());
```
