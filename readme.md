<h3>Version — 1.5</h3>
<h3>Minimum SDK — 2.2+</h3>

<h2>Install</h2>
You may import src from project (need delete example folder) or <a href="https://github.com/kvirair/Simple-Scanner-Android/releases">download jar</a> (recommended)
<br><br>
Don't forget done this:
<br>
— Copy folders **armeabi**, **armeabi-v7a**, **x86** and **zbar.jar** to your libs folder (<a href="http://zbar.sourceforge.net/">project url</a>)
<br>
— Copy **android-support-v4.jar** to your libs (<a href="http://developer.android.com/tools/support-library/setup.html">how setup</a>)

<h2>Quick start</h2>

— Create your activity with listener (don't forget add this activity to manifest)

```java
public class YourActivity extends FragmentActivity implements ScannerListener {

  @Override
  public void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.your_layout);

        SimpleScannerFragment simpleScannerFragment = (SimpleScannerFragment)
            getSupportFragmentManager().findFragmentById(R.id.scannerFragment);
        simpleScannerFragment.setScannerListener(this);

    }

  @Override
    public void onDataReceive(String data, int barcodeType) {
    // your code
  }

}
```

— And don't forget add fragment to your_layout, for example:

```java
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
                android:layout_width="fill_parent"
                android:layout_height="fill_parent">

   <fragment
        android:id="@+id/scannerFragment"
        android:layout_centerInParent="true"
        class="garin.artemiy.simplescanner.library.fragments.SimpleScannerFragment"
        android:layout_height="wrap_content"
        android:layout_width="wrap_content"/>

</RelativeLayout>
```

**That's all!** Enjoy.

<h2>Examples for scanning</h2>

![QR-Code](http://img208.imageshack.us/img208/4696/ors.gif)

<h2>License</h2>
```
Copyright (C) 2013 Artemiy Garin

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

