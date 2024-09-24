A package that facilitates the implementation of on scroll reveal animations in astro projects.

# Install:

`npm install astro-onscroll-animations`

---

### Usage Guide for OnScrollReveal Component

1. **Import the `OnScrollReveal` component** on the desired page.
2. **Add the `scroll-animation` class** to any HTML elements you want to animate on scroll.
3. **Add the animation class name: `scroll-animation-default` or `swing-in-left`** to specify the animation you want to use.
4. **Use delay classes (Optional)**, such as `delay-300`, to stagger the animation start time for sequential animations.

```astro
---
import OnScrollReveal from 'astro-onscroll-animations';
---

<body>
  <div class="hero">
        <h1 class="scroll-animation scroll-animation-default">Hello</h1>
        <h1 class="scroll-animation scroll-animation-default delay-300">World!</h1>
  </div>
  <div class="hero">
        <h2 class="scroll-animation swing-in-left delay-600">Text</h2>
        <h2 class="scroll-animation swing-in-left delay-750 ">Another Text</h2>
  </div>

  <!-- Initialize the OnScrollReveal functionality -->
  <OnScrollReveal />
</body>
```

### Key Points:

- **`scroll-animation`**: Attach this class to elements that should animate when they enter the viewport.
- **Animation Classes**: there are two animation classes available: `scroll-animation-default` and `swing-in-left`
  **_scroll-animation-default_**

  ```css
  .scroll-animation-default {
    transform: translateY(50px);
    opacity: 0;
    transition: all 0.5s ease-in;
  }

  .scroll-animated-default {
    transform: translateY(0);
    opacity: 1;
  }
  ```

  **_swing-in-left_**

  ```css
  .swing-in-left {
    animation: none;
  }

  .swing-in-left-anim {
    animation-name: swingAnim;
    animation-duration: 2s;
    animation-timing-function: ease;
    animation-fill-mode: forwards;
    animation-iteration-count: 1;
    opacity: 1;
  }

  @keyframes swingAnim {
    0% {
      opacity: 0;
      transform: rotateY(100deg);
      transform-origin: left;
    }

    100% {
      opacity: 1;
      transform: rotateY(0);
      transform-origin: left;
    }
  }
  ```

- **Delay Classes**: To create a sequence of animations, you can add delay classes like `delay-300`, `delay-600`, etc. The value represents the delay in milliseconds before the animation starts. Delay classes starts from delay-300 which indicated to delay 300ms to delay-1200, and available in 150ms intervals:

  - `delay-300` – 300ms delay
  - `delay-450` – 450ms delay
  - `delay-600` – 600ms delay
  - `delay-750` – 750ms delay
  - `delay-900` – 900ms delay
  - `delay-1050` – 1050ms delay
  - `delay-1200` – 1200ms delay

### Example:

- In this example, the first heading (`Hello`) animates immediately when it appears, while the second heading (`World!`) starts its animation 300ms later. (`Text`) and (`Another Text`) animates with the style of swing-in-left animation with corresponding delays.

This structured approach should make it easier to follow the guide and implement the `OnScrollReveal` component effectively.
