# Responsive Web Design
## Media Query
@media (max-width: 100px) { /* CSS Rules */ }

## Image Responsive
``` css
img {
  max-width: 100%;
  display: block;
  height: auto;
}
```

## Viewport Units
Viewport에 relative한 unit을 사용
```
vw: 10vw would be 10% of the viewport's width.
vh: 3vh would be 3% of the viewport's height.
vmin: 70vmin would be 70% of the viewport's smaller dimension (height vs. width).
vmax: 100vmax would be 100% of the viewport's bigger dimension (height vs. width).
```