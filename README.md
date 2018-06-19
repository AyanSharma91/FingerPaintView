# FingerPaintView

**Android library to draw or paint using different brushes.**


Brushes available are:
>1.Neon brush
>2.Fade brush
>3.Glow brush
>4.Blur brush
>5.Emboss brush
>6.Deboss brush


#Screenshot

<img src="images/s1.png" width="360" height="640" />   <img src="images/neon.png" width="360" height="640" />   <img src="images/glow.png" width="360" height="640" />   <img src="images/fade.png" width="360" height="640" />   <img src="images/emboss.png" width="360" height="640" />   <img src="images/deboss.png" width="360" height="640" />   <img src="images/blur.png" width="360" height="640" />   <img src="images/object.png" width="360" height="640" />  



#Sample usage

```

DrawableOnTouchView drawableOnTouchView = new DrawableOnTouchView(this);
            drawableOnTouchView.setActionListener(new DrawableOnTouchView.OnActionListener() {
                @Override
                public void OnCancel() {
                            drawableOnTouchView.setClickable(false);

                }

                @Override
                public void OnDone(Bitmap bitmap) {
                            drawableOnTouchView.makeNonClickable(false);
                }

                @Override
                public void show() {
                        drawableOnTouchView.makeNonClickable(true);
                }

                @Override
                public void killSelf() {
                    //if(listener!=null)listener.killSelf(drawableOnTouchView.getBitmap());
                }
            });

            drawableOnTouchView.setColorChangedListener(new DrawableOnTouchView.OnColorChangedListener() {
                @Override
                public void onColorChanged(int color) {

                }

                @Override
                public void onStrokeWidthChanged(float strokeWidth) {

                }

                @Override
                public void onBrushChanged(int Brushid) {

                }
            });
            drawableOnTouchView.attachCanvas();

            FrameLayout.LayoutParams params=new FrameLayout.LayoutParams(ViewGroup.LayoutParams.MATCH_PARENT, ViewGroup.LayoutParams.MATCH_PARENT);
            params.gravity= Gravity.CENTER;

            mainFrame.addView(drawableOnTouchView,params);


```

>Todo: Add documentation.