# sfviewpager
SFViewpager is a customize view for viewpager in jar library.<br />
<br />

### Screen
![alt text](https://raw.githubusercontent.com/Saeed-7/sfviewpager/master/screen/sfViewpager.gif)
<br />
### How to use
1- Download jar file and copy into lib folder in your project.<br />
2- Use below custom RelativeLayout in your layout:</ br>
```
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
2.1- Add appNs in your attribute:</ br>
```
        xmlns:app="http://schemas.android.com/apk/res-auto"
```
2.2- Use 'title_size' attribute for text-size of TabLayout.</ br>
2.3- Use 'spacer_line_height' attribute for height of line between tablayout and viewpager.(you can use '0')</ br>
2.4- Use 'tab_height' attribute for normal height of tabs in tablayout.</ br>
2.5- Use 'tab_height_max' attribute for height of select tab in tablayout.</ br>
2.6- Use 'icon_size' attribute for size of icon drawable.</ br>
</ br>
3- Get references of SfViewpager in your Activity (or Fragment).</ br>
```
        SFViewpager sfViewPager = (SFViewpager) findViewById(R.id.sfViewpager);
```
4- Get object from 'SFViewpagerModel' for each tab like below:</ br>
```
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
5- Put all 'SFViewpagerModel's into the List:</ br>
```
        List<SFViewpagerModel> models = new ArrayList<>();
        models.add(0, model_1);
        models.add(1, model_2);
        models.add(2, model_3);
        ...
```
6- Call 'setup' method:</ br>
```
        sfViewPager.setup(
                      Activity activity, // In Activities use 'this', and in Fragments use 'getActivity()'.
                      int countOfTabs, // Number of tabs.
                      List<SFViewpagerModel> models // Put above List<SFViewpagerModel> here.
                      );
```
7- Injoy.

### Contact me: en.SaeedFekri@gmail.com
