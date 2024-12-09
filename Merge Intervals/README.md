<h1> Merge Intervals :</h1>
Given an array of time intervals where <b>arr[i] = [start<sub>i</sub>, end<sub>i</sub>].</b>
<h1>Task :</h1>
Merge all the <B>overlapping intervals</B> into one and The result which should have only <b>Mutually Exclusive intervals</b>.
<h1> Example :</h1>

![Merge Overlapping Intervals](https://www.interviewbit.com/blog/wp-content/uploads/2021/11/merge-overlapping-intervals-951x1024.png)

<h3> Steps to solve : </h3>
<ul>
  <li>  First sort the intervals based on their starting points </li>
  Eg . [(1,4),(7,9),(3,6),(8,10)]
  <ul>
     After Sorting on basis of Starting Postion.
  </ul>
  <ul>
    [(1,4),(3,6),(7,9),(8,10)]
  </ul>
   <ul>
     Disclaimer :
   </ul>
   <ul>
     if Intervals 's starting Postion have same value then Sorting will be based on their Ending Points.
   </ul>
  <ul>
    Eg . [(1,4),(7,9),(3,6),(7,3),(8,10)]
  </ul>
  <ul>
    After Sorting
  </ul>
  <ul>
    [(1,4),(3,6),(7,3),(7,9),(8,10)]
  </ul>
</ul>
