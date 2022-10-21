
## Usage
- Add ImageSlider to your **layout**
```xml
<com.denzcoskun.imageslider.ImageSlider
        android:id="@+id/image_slider"
        android:layout_width="wrap_content"
        android:layout_height="300dp"
        app:auto_cycle="true"
        app:corner_radius="20"
        app:period="1000"
        app:delay="0"/>
```
- You can change indicators.
```xml
app:selected_dot="@drawable/default_selected_dot"
app:unselected_dot="@drawable/default_unselected_dot"
```
- Add ImageSlider to your **Activity**
```kt
val imageList = ArrayList<SlideModel>()
	// imageList.add(SlideModel("String Url" or R.drawable)
	// imageList.add(SlideModel("String Url" or R.drawable, "title") Also you can add title
        imageList.add(SlideModel("https://1.bp.blogspot.com/-GUZsgr8my50/XJUWOhyHyaI/AAAAAAAABUo/bljp3LCS3SUtj-judzlntiETt7G294WcgCLcBGAs/s1600/fox.jpg", "Twin foxes"))
        imageList.add(SlideModel("https://2.bp.blogspot.com/-CyLH9NnPoAo/XJUWK2UHiMI/AAAAAAAABUk/D8XMUIGhDbwEhC29dQb-7gfYb16GysaQgCLcBGAs/s1600/tiger.jpg"))
        imageList.add(SlideModel("https://3.bp.blogspot.com/-uJtCbNrBzEc/XJUWQPOSrfI/AAAAAAAABUs/ZlReSwpfI3Ack60629Rv0N8hSrPFHb3TACLcBGAs/s1600/elephant.jpg", "Alone Elephant"))
        val imageSlider = findViewById<ImageSlider>(R.id.image_slider)
        imageSlider.setImageList(imageList)
```
- You can use click listener. 
```kt
imageSlider.setItemClickListener(object : ItemClickListener {
    override fun onItemSelected(position: Int) {
	// You can listen here
    }
})
```
## Setup
```xml
allprojects {
    repositories {
        ...
        maven { url 'https://jitpack.io' }
    }
}

dependencies {
	implementation 'com.github.denzcoskun:ImageSlideshow:0.0.2'
}
