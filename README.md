# Welcome Test Todo
Temporary Todo Project


## About

This is a **temporary** library for `todo` project.

### Quick Start

1 - Implements model mapping

~~~ bash

protected override void OnModelCreating(ModelBuilder modelBuilder)
{
    base.OnModelCreating(modelBuilder);
    modelBuilder.UseFactoryMapping();
}
~~~

2 - Implements with dependency injection for all services and workers.

~~~ bash
using Factory.Worker.Public.DependencyInjection;


public static IServiceCollection ConfigureServices(HostBuilderContext hostContext, IServiceCollection services){
    services.UseFactoryWorker<FactoryDbContext, Factory, Guid>(x => x);
}
~~~

## Notes

For more, you can check out for the `Factory.Todo` project
