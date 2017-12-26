# css gradients

[linear-gradient](https://developer.mozilla.org/zh-CN/docs/Web/CSS/linear-gradient)

## less

```less
.gradients(@type;@angle;@color) when(@type = linear) {
    background-image: -webkit-linear-gradient(unit((90-@angle),deg), @color);
    background-image: linear-gradient(unit(@angle,deg), @color);
}

.gradients(@type;@shape;@color) when(@type = radial) {
    background-image: -webkit-radial-gradient(@shape,@color);
    background-image: radial-gradient(@shape,@color);
}
```

### tags

```less
.gradient-tag {
  &.blue {
    .gradients(linear;
    140;
    #65bfff, #1280ff);
  }
  &.orange {
    .gradients(linear;
    140;
    #feca1e, #ff9f00);
  }
  &.green {
    .gradients(linear;
    140;
    #9ddc33, #71c812);
  }
  &.pink {
    .gradients(linear;
    140;
    #ff8f99, #f64a64);
  }
}
```

### book spine

```less
@spine: rgba(0,0,0,.15),rgba(0,0,0,.08) 3%,rgba(255,255,255,.2),rgba(0,0,0,.15),rgba(0,0,0,.03) 5%, rgba(0, 0, 0, 0);
.gradient(linear, 90, @spine);
```



