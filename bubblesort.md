<h1><i>BUBBLE SORT<i></h1>
<p>Bubble Sort is the simplest sorting algorithm that works by repeatedly swapping the adjacent elements if they are in wrong order.</p>
<h2>More on bubble sort</h2>
<p>Bubble sort, sometimes referred to as sinking sort, is a simple sorting algorithm that repeatedly steps through the list to be sorted, compares each pair of adjacent items and swaps them if they are in the wrong order. The pass through the list is repeated until no swaps are needed, which indicates that the list is sorted. The algorithm, which is a comparison sort, is named for the way smaller or larger elements "bubble" to the top of the list. Although the algorithm is simple, it is too slow and impractical for most problems even when compared to insertion sort.[2] It can be practical if the input is usually in sorted order but may occasionally have some out-of-order elements nearly in position.</p>
<h2>A function is C to implement Bubble Sort</h2>
<pre><code>
void bubbleSort(int arr[], int n)
{
   int i, j;
   for (i = 0; i < n-1; i++)      
 
       // Last i elements are already in place   
       for (j = 0; j < n-i-1; j++) 
           if (arr[j] > arr[j+1])
              swap(&arr[j], &arr[j+1]);
}
</code></pre>
<h2>Psuedo Code</h2>
<pre><code>
procedure bubbleSort( A : list of sortable items )
    n = length(A)
    repeat 
        swapped = false
        for i = 1 to n-1 inclusive do
            /* if this pair is out of order */
            if A[i-1] > A[i] then
                /* swap them and remember something changed */
                swap( A[i-1], A[i] )
                swapped = true
            end if
        end for
    until not swapped
end procedure
</code></pre>
<h2>Complexity</h2>
<p>Worst and Average Case Time Complexity: O(n*n). Worst case occurs when array is reverse sorted.

Best Case Time Complexity: O(n). Best case occurs when array is already sorted.

Auxiliary Space: O(1)

Boundary Cases: Bubble sort takes minimum time (Order of n) when elements are already sorted.

Sorting In Place: Yes

Stable: Yes</p>
<h2>Applications</h2>
<p>For beginners to just understand the concept of sorting</p>
<h2>Conclusion</h2>
<p>This technique of sorting should be used only for small inputs or to understand the concept of sorting.There are much better sorting techniques which will be uploaded soon</p>
