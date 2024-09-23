A package that facilitates the implementation of on scroll reveal animations in astro projects.

# Install:

`npm install astro-onscroll-animations`


---

### Usage Guide for OnScrollReveal Component

1. **Import the `OnScrollReveal` component** on the desired page.
2. **Add the `scroll-animation` class** to any HTML elements you want to animate on scroll.
3. **Use delay classes**, such as `delay-300`, to stagger the animation start time for sequential animations.

```astro
---
import OnScrollReveal from 'astro-onscroll-animations';
---

<body>
  <div class="hero">
    <h1 class="scroll-animation">Hello</h1>
    <h1 class="scroll-animation delay-300">World!</h1>
  </div>
  
  <!-- Initialize the OnScrollReveal functionality -->
  <OnScrollReveal />
</body>
```

### Key Points:
- **`scroll-animation`**: Attach this class to elements that should animate when they enter the viewport.
- **Delay Classes**: To create a sequence of animations, you can add delay classes like `delay-300`, `delay-600`, etc. The value represents the delay in milliseconds before the animation starts.

### Example:
- In this example, the first heading (`Hello`) animates immediately when it appears, while the second heading (`World!`) starts its animation 300ms later.

This structured approach should make it easier to follow the guide and implement the `OnScrollReveal` component effectively.



