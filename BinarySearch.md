<h1><i>Binary Search<i></h1>>
<p>Binary search is the most popular Search algorithm.It is efficient and also one of the most commonly used techniques that is used to solve problems.
</p>
<h2>Finding a value in a sorted sequence</h2>
<p>In its simplest form, binary search is used to quickly find a value in a sorted sequence (consider a sequence an ordinary array for now). We’ll call the sought value the target value for clarity. Binary search maintains a contiguous subsequence of the starting sequence where the target value is surely located. This is called the search space. The search space is initially the entire sequence. At each step, the algorithm compares the median value in the search space to the target value. Based on the comparison and because the sequence is sorted, it can then eliminate half of the search space. By doing this repeatedly, it will eventually be left with a search space consisting of a single element, the target value.
</p>
<h2>Psuedo code:</h2>
<pre><code>
binary_search(A, target):
   lo = 1, hi = size(A)
   while lo <= hi:
      mid = lo + (hi-lo)/2
      if A[mid] == target:
         return mid     
      else if A[mid] < target: 
         lo = mid+1
      else:
         hi = mid-1
            
   // target was not found
</code></pre>
<h2>C++ Implementation:</h2>
<pre><code>
int binarySearch(int* arr,int l,int r,int x)
{
   if(r>=l)
   {
        int mid=l+(r-l)/2;<br>
        if(arr[mid]==x) 
        return mid;
        if(arr[mid]>x)
        return binarySearch(arr,l,mid-1,x);
        return binarySearch(arr,mid+1,r,x);
   }
   return -1;
}
</code></pre>
<h2>Complexity:</h2>
<p>Since each comparison binary search uses halves the search space, we can assert and easily prove that binary search will never use more than (in big-oh notation) O(log N) comparisons to find the target value.The logarithm is an awfully slowly growing function
<br>
In case you’re not aware of just how efficient binary search is,If you could manage a list containing all the people in the world sorted by name, you could find any person in less than 35 steps
</p>
<h2>Limitations:</h2>
<p>It requires the given data structure to be accessible continuosly and easily
Also it requires that the data is arranged monotonically.
</p>
<h2>Applications:</h2>
<p> now as you may think what other purpose could binary SEARCH serve other than searching but as such it has a wide range of applications
<ul>
<li>Searching Ordered Data (obvious)</li>
<li>Finding the value for which a given monotonic function assumes a particular value</li>
<li>debugging a somewhat linear piece of code. if the code has many steps mostly executed in a sequence and there's a bug, you can isolate the bug by finding the earliest step where the code produces results which are different from the expected ones.</li>
</ul>
<h2>Problems:</h2>
<p>
<ul>
<li><a href="https://www.codechef.com/problems/CHNGSS">Chef and Number Guessing</a></li>
<li><a href="https://www.codechef.com/problems/TRICOIN">Coins And Triangle</a></li>
<li><a href="https://www.codechef.com/problems/SNAKEEAT">Snake Eating</a></li>
<li><a href="https://www.codechef.com/problems/FORESTGA">Forest Gathering</a></li>
</ul>
</p>
</p>
<p>As such binary search appears to be a very primary search technique but it is highly efficient and can be used at several places to find solution where binary search may not strike as an intutive method as such</p>
