# sfviewpager
SFViewpager is a customize view for viewpager in jar library.


## Screen
![alt text](https://raw.githubusercontent.com/Saeed-7/sfviewpager/master/screen/sfViewpager.gif)

## How to use
1. Download jar file and copy into lib folder in your project.
2. Use below custom RelativeLayout in your layout:
```xml
<ir.saeed7.sfviewpager.SFViewpager
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        xmlns:app="http://schemas.android.com/apk/res-auto"
        android:layout_marginTop="40dp"
        android:id="@+id/sfViewpager"
        app:title_size="20"
        app:spacer_line_height="20"
        app:tab_height="40"
        app:tab_height_max="60"
        app:icon_size="36"/>
        ```
  * Add appNs in your attribute:  
```xmlns:app="http://schemas.android.com/apk/res-auto"
```

  * Use 'title_size' attribute for text-size of TabLayout.
  * Use 'spacer_line_height' attribute for height of line between tablayout and viewpager.(you can use '0')
  * Use 'tab_height' attribute for normal height of tabs in tablayout.
  * Use 'tab_height_max' attribute for height of select tab in tablayout.
  * Use 'icon_size' attribute for size of icon drawable.

3. Get references of SfViewpager in your Activity (or Fragment).
```
        SFViewpager sfViewPager = (SFViewpager) findViewById(R.id.sfViewpager);
```
4. Get object from 'SFViewpagerModel' for each tab like below:
```java
        new SFViewpagerModel(
                        int topLineColor, // When select this tab, SpacerLine's color change to this color.
                        int iconImageResource, // Path or resource of icon. (use by Glide)
                        String title, // Title of tab
                        int titleColor, // Text-color of title
                        Drawable background, // Drawable for TabBackground
                        Fragment fragment, // Fragment for viewpager
                        Typeface titleFontFace // Typeface for title if you want, you can use 'null'.
                        )
```
5. Put all 'SFViewpagerModel's into the List:
```java
        List<SFViewpagerModel> models = new ArrayList<>();
        models.add(0, model_1);
        models.add(1, model_2);
        models.add(2, model_3);
        ...
```
6. Call 'setup' method:
```java
        sfViewPager.setup(
                      Activity activity, // In Activities use 'this', and in Fragments use 'getActivity()'.
                      int countOfTabs, // Number of tabs.
                      List<SFViewpagerModel> models // Put above List<SFViewpagerModel> here.
                      );
```
7. Injoy.
```
```
## Contact me: en.SaeedFekri@gmail.com
