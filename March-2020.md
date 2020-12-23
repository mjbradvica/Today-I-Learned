# 3/5
Id's take precedence over classes in CSS  

CSS Precedence rules:

1. !important
2. Specificty of css rule selectors
3. Sequence of declaration

# 3/7

Javascript whell events responds to the mousewheel  
The whell event uses a deltaY property for up or down  
You can use the whell event + viewHeight to have controlled scrolling  

```typescript
//To Get ViewHeight
const viewHeight = Math.max(document.documentElement.clientHeight, window.innerHeight || 0);

document.addEventListener("wheel", (event: WheelEvent) => {
        if (event.deltaY > 0) {
            window.scrollBy(0, viewHeight);
        } else {
            window.scrollBy(0, -viewHeight);
        }
    });
```

CSS to enable smooth scrolling

```css
html { scroll-behavior: smooth; } 
```  

Font families are applied to the body tag, not the html tag  

# 3/9

.NET Type constrains behavior in accordance to class inheritance  
You can only have a single class constriant, but multiple interfaces  
Order of constraints matters - class, interfaces, new()  

```csharp
public interface IPerson<T> where T : Entity, IEntity, IEquality, new()
```

# 3/13

React uses the forHtml tag instead of for tag for labels  

```html
<label htmlFor="input"></label>
<input id="input"></input>
```  

# 3/15

You don't need the Microsoft.Extensions.DepedencyInjection package to use the default .NET Core DI

Lifetimes available:

1. Singleton - One instance  
2. Scoped - One instance per http request  
3. Transient - Instance per request  

Features not supported:  

1. Property Injection  
2. Injection based on name  
3. Child containers  
4. Custom lifetimes  
5. Lazy initialization  

DbContexts should use a scoped lifetime.  
You can manually wire up dependencies by using the ServiceDescriptor class  
The IServiceProvider interface can be used to obtain existing dependencies  
