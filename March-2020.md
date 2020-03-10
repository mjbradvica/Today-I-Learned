# Today I Learned 2020

# 3/5/2020
Id's take precedence over classes in CSS  

CSS Precedence rules:
1. !important
2. Specificty of css rule selectors
3. Sequence of declaration

# 3/7/202
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

# 3/9/10

.NET Type constrains behavior in accordance to class inheritance  
You can only have a single class constriant, but multiple interfaces  
Order of constraints matters - class, interfaces, new()  

```csharp
public interface IPerson<T> where T : Entity, IEntity, IEquality, new()
```
