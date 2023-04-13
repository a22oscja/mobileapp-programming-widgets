
# Rapport


Initially upon opening the program a constraintLayout and a textview were present.
A linearLayout was added with the following code, the end of the linearLayout is excluded here
as the linearLayout itself includes other widgets:
```
    <LinearLayout
        android:layout_width="120dp"
        android:layout_height="400dp"
        android:orientation="vertical"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toEndOf="@+id/textView"
        app:layout_constraintTop_toTopOf="parent">
```
This layout has its constraints being top, bottom and right of its parent, being the initial constraintLayout.
As well as one to the left being the initial textview, this results in the layout
being position in the middle vertically and between the textview and the right of the screen horizontally.

the next part of the assignment was to add three different widgets inside this layout.
For this i decided upon using two of the given example widgets, button and editText, together
with one not given as example, being progressBar.

first the editText widget was added:
```
    <EditText
            android:id="@+id/hello"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginVertical="30dp"
            android:background="@color/colorAccent"
            android:inputType="number"
            android:minHeight="48dp"
            android:text="hi" />
```
The basic setup for these widgets include making their alloted space equal
the width of its parent, while height of the alloted space can stay whatever size it
prefers, this is done with match parent and wrap content respectively. This is
done for all widgets.

Other than this, the editText field recieves some basic styling with a margin, background, and some text.
as well as specifying an input type number.

A progress bar is added:
```
        <ProgressBar
            android:id="@+id/progressBar"
            style="?android:attr/progressBarStyleHorizontal"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginVertical="30dp"
            android:background="#000"
            android:text="hi"
            android:max="100"
            android:progress="80"
            android:indeterminate="true"
            android:minHeight="48dp" />
```
Outside of the basic styling, a progressbar also recieves a progress value.
As it would be slightly overkill to implement something in java to fill this bar,
the bar is slightly filled by default and set to move with indeterminate.

Lastly a button is added:
```
        <Button
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="press for nothing"
            android:layout_margin="10dp"
            android:padding="5dp"
            android:drawableRight="@drawable/abc_vector_test" />
```
The button recieves quite basic styling and a basic picture of an arrow that exists by default in
Android Studio.