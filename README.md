# ![Logo](https://github.com/freelancermustakin/IslamicPrayerTimes/blob/main/assets/mecca%2032x32.png?raw=true) Islamic Prayer Times
Know the exact duration of Namaz according to the coordinates taken from the browser.

``ব্রাউজার থেকে নেওয়া স্থানাঙ্ক অনুসারে নামাজের সঠিক সময়কাল জানুন। অফলাইনেও কাজ করে। হাইলাইট করা সারি বর্তমান নামাজের সময় খুঁজে পাওয়া সহজ করে তোলে। আপনি পরবর্তী নামাজের সময়ের অবশিষ্ট সময়ও পরীক্ষা করতে পারেন।``

### Features!
- Works offline.
- Highlited row makes easy to find the current prayer time.
- Android Studio application support.
- You may also check the remaining time of the next prayer time.
- Know you the exact prayer time duration according to the coordinates taken from the browser.
- English & Bengali langugae support.

### Upcomming Features!
  - Sahri and Iftar calendar.
  - More.

### Screenshot
![screenshot](assets/screenshot/pc_webview.png)
| | |
|:-------------------------:|:-------------------------:|
| <img src="assets/screenshot/phone_screenshot_205915.jpg" /> | <img src="assets/screenshot/phone_screenshot_205916.jpg" /> |

# Android Studio
> - XML android
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    tools:context=".SalahActivity">

    <WebView
        android:id="@+id/IslamicPrayerTimes"
        android:layout_width="match_parent"
        android:layout_height="match_parent" />

</LinearLayout>
```

> - Java android
```
package com.freelancermustakin.countdownbanglaclock;

import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import com.freelancermustakin.countdownbanglaclock.databinding.ActivitySalahBinding;

public class SalahActivity extends AppCompatActivity {

    ActivitySalahBinding aladaAppBinding;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        aladaAppBinding = ActivitySalahBinding.inflate(getLayoutInflater());
        setContentView(aladaAppBinding.getRoot());

        //bengali and english prayer times
        aladaAppBinding.IslamicPrayerTimes.getSettings().setJavaScriptEnabled(true);
        aladaAppBinding.IslamicPrayerTimes.getSettings().setLoadsImagesAutomatically(true);
        aladaAppBinding.IslamicPrayerTimes.getSettings().setJavaScriptCanOpenWindowsAutomatically(true);
        aladaAppBinding.IslamicPrayerTimes.loadUrl("file:///android_asset/IslamicPrayerTimes/index.html"); //load salah times

    }//end onClick
}
```

### Credits
- [aladhan-api](https://aladhan.com/prayer-times-api)
- [PrayTimes.org](http://praytimes.org/)
- [Moment.js](https://momentjs.com/)

### Author
- Developer by: [Freelancer Mustakin](https://freelancermustakin.github.io/)

### License
Prayer Times licensed under the  [MIT License]().
