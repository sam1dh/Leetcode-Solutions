<h1> Merge Intervals :</h1>
Given an array of time intervals where <b>arr[i] = [start<sub>i</sub>, end<sub>i</sub>].</b>
<h1>Task :</h1>
Merge all the <B>overlapping intervals</B> into one and The result which should have only <b>Mutually Exclusive intervals</b>.
<h1> Example :</h1>

![example](carbon.png)
![Merge Overlapping Intervals](https://www.interviewbit.com/blog/wp-content/uploads/2021/11/merge-overlapping-intervals-951x1024.png)

<h2> Steps to solve : </h2>
<ul>
 <h3>
  <ul>
    <li>First, sort the intervals based on their starting points.</li>
    <p>Example: [(1,4),(7,9),(3,6),(8,10)]</p>
    <ul>
      <li>After sorting based on the starting position:</li>
      <ul>
        <li>[(1,4), (3,6), (7,9), (8,10)]</li>
      </ul>
    </ul>

  <ul>
      <li><b>Disclaimer:</b></li>
      <ul>
        <li>If intervals' starting positions have the same value, then sorting will be based on their ending points.</li>
      </ul>
    </ul>

   <p>Example: [(1,4),(7,9),(3,6),(7,3),(8,10)]</p>
    <ul>
      <li>After sorting:</li>
      <ul>
        <li>[(1,4), (3,6), (7,3), (7,9), (8,10)]</li>
      </ul>
    </ul>

  <li>After sorting, this allows us to easily identify <b>overlapping intervals</b> by comparing each interval with the last merged interval.</li>
    
  <ul>
        
      <p>Example: [(1,4), (3,6), (7,3), (7,9), (8,10)]</p>
      <ul>
        <li>Now check at Index: 0</li>
        <ul>
          <li>(1,4)</li>
        </ul>
      </ul>
    </ul>
  </ul>
</h3>

</ul>
