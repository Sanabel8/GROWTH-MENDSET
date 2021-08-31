## Create dynamic lists with RecyclerView

- RecyclerView recycles those individual elements. When an item scrolls off the screen, RecyclerView doesn't destroy its view.
- Besides being the name of the class, RecyclerView is also the name of the library. In this page, RecyclerView in code font always means the class in the RecyclerView library

## Key classes

1. RecyclerView
2. Each individual element in the list is defined by a view holder object.
3. The RecyclerView requests those views
4. The layout manager arranges the individual elements in your list.

## Steps for implementing your RecyclerView

1. decide what the list or grid is going to look like
2. Design how each element in the list is going to look and behave. Based on this design, extend the ViewHolder class.
3. Define the Adapter that associates your data with the ViewHolder views.

## Plan your layout

- The items in your RecyclerView are arranged by a LayoutManager class
- the most common layout situations:

1. LinearLayoutManager arranges the items in a one-dimensional list.
2. GridLayoutManager arranges all items in a two-dimensional grid
3. StaggeredGridLayoutManager is similar to GridLayoutManager

## Implementing your adapter and view holder

- When you define your adapter, you need to override three key methods:

1. onCreateViewHolder()
2. onBindViewHolder()
3. getItemCount()

- The layout for the each view item is defined in an XML layout file, as usual. In this case, the app has a text_row_item.xml file like this:

```<FrameLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="@dimen/list_item_height"
    android:layout_marginLeft="@dimen/margin_medium"
    android:layout_marginRight="@dimen/margin_medium"
    android:gravity="center_vertical">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/element_text"/>
  </FrameLayout>
```
