The **render cycle** happens *after* JS execution and before the browser paints the frame.
Every time you change something on the page — like move a box, change a color, or type in a form — the browser **"renders"** (draws) the new screen. That drawing process is called the **Render Cycle**.

## What happens when your code runs?

When JavaScript changes the page (like changing colors, sizes, positions), the browser goes through **these steps**:

```
1. Run JavaScript (your code)
2. Check what styles changed (CSS stuff)
3. Measure and calculate where things are (layout)
4. Draw the pixels (paint)
5. Combine everything together (composite)
6. Show it on the screen
```

## Tools for Analyzing Render Cycles

1. **Chrome DevTools > Performance Tab**
    - Record → Interact → Stop
    - Inspect frames, layout, paint, JS timings
2. **Lighthouse** (Performance Audit)
3. **FPS Meter** in Chrome (Experimental)
4. **Firefox Performance Panel**


## Summary ::::

- Your code changes the page → browser must update screen.
- The browser goes through steps: JS → Style → Layout → Paint → Composite.
- Too many updates or bad timing (reading and writing together) = slow.
- Use `requestAnimationFrame()` to do smooth changes.
- Use `transform` and `opacity` for fast animations (they skip most slow steps).