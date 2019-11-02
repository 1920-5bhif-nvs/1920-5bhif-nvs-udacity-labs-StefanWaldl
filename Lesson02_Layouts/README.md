## Lesson 02: Layouts - Tripi&#x0107; Nenad

**Contents:**

 - Explanation of basic layouts
 - Layout Editor basics
 - Styling
 - dimens.xml - a file which stores all dimensons e.g. for texts
 - Extract styles
 - Editable textview
 - Visibility depends on something
 - Data Binding


## Key takeaways - What was new for me?

### Data Binding
Before you can use it, you have to enable it. Therefore go to `build.gradle (Module: app)` in `android{}` and append following: ```dataBinding {enabled = true}```

#### Data Binding - The Idea

-   The big idea about data binding is to create an object that connects/maps/binds two pieces of distant information together at compile time, so that you don't have to look for it at runtime.
-   The object that surfaces these bindings to you is called the Binding object. It is created by the compiler, and while understanding how it works under the hood is interesting, it is not necessary to know for basic uses of data binding.

#### Data Binding and findViewById

-   findViewById is a costly operation because it traverses the view hierarchy every time it is called.
-   With data binding enabled, the compiler creates references to all views in a `<layout>` that have an id, and gathers them in a Binding object.
-   In your code, you create an instance of the binding object, and then reference views through the binding object with no extra overhead.

![enter image description here](https://video.udacity-data.com/topher/2018/November/5be384c4_4704sc-a-layoutsdata-binding-intro-slide/4704sc-a-layoutsdata-binding-intro-slide.png)
#### Data Binding Views and Data
![enter image description here](https://video.udacity-data.com/topher/2018/November/5be384d1_l2-5203sc-alayoutsdata-binding-data-slide/l2-5203sc-alayoutsdata-binding-data-slide.png)

## User-Interface
![alt text](screenshots/screenshot01.png)


