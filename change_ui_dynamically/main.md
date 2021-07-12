## 代码动态修改 UI

- 1.修改控件的 drawable 资源（background 属性，引用了 shape，改变 stroke 颜色）
- 修改 drawable 的 svg 矢量图资源颜色



---

#### 1. 修改控件的 drawable 资源（background 属性，引用了 shape，改变 stroke 颜色）

```java
 Button btn = findViewById(R.id.btn);
 Drawable btnBackground = btn.getBackground();
 if (btnBackground instanceof GradientDrawable){
     GradientDrawable gradientDrawable = (GradientDrawable) btnBackground;
     gradientDrawable.setStroke(2, your new color value);
 }
```

#### 2. 修改 drawable 的 svg 矢量图资源颜色

```java
// 前提：ImageView 用 src 属性，引用了 矢量图资源
ImageView iv = findViewById(R.id.iv);
iv.setColorFilter(your new color value, PorterDuff.Mode.SRC_IN);
```

