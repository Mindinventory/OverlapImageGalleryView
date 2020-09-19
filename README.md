# OverlapImageGalleryView
[![](https://jitpack.io/v/Mindinventory/OverlapImageGalleryView.svg)](https://jitpack.io/#Mindinventory/OverlapImageGalleryView)

## Overview

OverlapImageGalleryView is a flexible library which helps you to create overlapping images gallery in your android Application. You can easily integrate it with the most popular image loading libraries such as Picasso, Glide and Fresco.


### Preview

![image](/media/AnimOverlapImageGalleyView.gif)


### Key features

* Easy way to integrate it with your recyclerview adapter.
* Overlapping space as you want.
* Number of items to show in gallery as overlapped.
* Different scroll animations.
* Orientation.
* Supported androidx


# Usage

* Dependencies

    Step 1. Add the JitPack repository to your build file:
    
    Add it in your root build.gradle at the end of repositories:

    ```groovy
	    allprojects {
		    repositories {
			    ...
			    maven { url 'https://jitpack.io' }
		    }
	    }
    ```


    Step 2. Add the dependency
    ```groovy
	    dependencies {
		    implementation 'com.github.Mindinventory:OverlapImageGalleryView:1.0.2'
	    }
    ```

```Fragment/Activity
    //------limit number of items to be overlapped     
    private val overlapLimit = 5     
  
    //------set value of item overlapping in percentage between 0 to 100
    private val overlapWidthInPercentage = -50
  
    //------set item decoration for item overlapping
    recyclerView.addItemDecoration(OverlapRecyclerViewDecoration(overlapLimit, overlapWidth))
    recyclerView.adapter = mAdapter         
    mAdapter.setImageList(setDummyArrayList())
    
    
    //------ Implement OverlapRecyclerViewClickListener interface to get callback of items click.
    override fun onNormalItemClicked(adapterPosition: Int) {
        toast(this,"Normal item clicked >> $adapterPosition")
    }

    override fun onNumberedItemClick(adapterPosition: Int) {
        toast(this,"Numbered item clicked >> $adapterPosition")
        // Here you can add remaining items in list or open seperate screen.
    }
    

```
#### Other lib which we have used here
* Glide -> implementation 'com.github.bumptech.glide:glide:4.8.0'

### Dribbble
https://dribbble.com/shots/5790365-Magnetic-Swipe-Animation-code

# LICENSE!

OverlapImageGalleryView is [MIT-licensed](/LICENSE).

# Let us know!
We’d be really happy if you send us links to your projects where you use our component. Just send an email to sales@mindinventory.com And do let us know if you have any questions or suggestion regarding our work.
