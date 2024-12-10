<h1> Merge Intervals :</h1>
Given an array of time intervals where <b>arr[i] = [start<sub>i</sub>, end<sub>i</sub>].</b>
<h1>Task :</h1>
Merge all the <B>overlapping intervals</B> into one and The result which should have only <b>Mutually Exclusive intervals</b>.
<h1> Example :</h1>

![example](carbon.png)
<img src="https://www.interviewbit.com/blog/wp-content/uploads/2021/11/merge-overlapping-intervals-951x1024.png" alt="Merge Overlapping Intervals" width="450">

<h2> Steps to solve : </h2>
<ul>
  <ul>
    <li>First, Sort the intervals based on their starting points.</li>
       
   <img src="https://www.interviewbit.com/blog/wp-content/uploads/2021/11/contagious-fashion-1024x382.png" alt="example" width="450">
     <li><b>Disclaimer:</b></li>
     <li>If Intervals' starting positions have the same value, then sorting will be based on their ending points.</li>   
    <img src="Index.png" alt="example" width="450" height = "300">    
  </ul>
  <ul>
   <li>After Sorting , It will be easy to Merge intervals by comparing the end point of first interval and Start point of Second Interval </b>.</li>
   <img src="" alt="example" width="450" height = "300">
    <li>  This allows us to easily identify overlapping intervals by comparing each interval with the last merged interval </li>
  </ul>

</ul>
  

       
