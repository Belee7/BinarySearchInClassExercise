Binary Search In Class Exercise
===============================
1. Copy and paste the following code into Processing
public void setup() {            
  int [] theArray = {1, 3, 5, 7, 10};           
  System.out.print(binarySearch(theArray, 0)+", ");            
  System.out.print(binarySearch(theArray, 1)+", ");            
  System.out.print(binarySearch(theArray, 3)+", ");            
  System.out.print(binarySearch(theArray, 6)+", ");            
  System.out.print(binarySearch(theArray, 10)+", ");            
  System.out.println(binarySearch(theArray, 11));          
  System.out.print(binarySearch(theArray, 0, 0, 4)+", ");            
  System.out.print(binarySearch(theArray, 1, 0, 4)+", ");            
  System.out.print(binarySearch(theArray, 3, 0, 4)+", ");            
  System.out.print(binarySearch(theArray, 6, 0, 4)+", ");            
  System.out.print(binarySearch(theArray, 10, 0, 4)+", ");            
  System.out.println(binarySearch(theArray, 11, 0, 4));
}      
public static int binarySearch(int [] naNums, int nTarget) {           
   int high = naNums.length-1;
  int low = 0;
  while (high>=low)
  {
    int guess =(low + high)/2 ;
    if (naNums[guess] == nTarget)
    return guess;
    else if (naNums[guess] < nTarget)
    low = guess+1;
    else
    high = guess-1;
    
  }
  return -1;
}      
public static int binarySearch(int [] naNums, int nTarget, int low, int high) {           
   int guess =(low + high)/2 ;
   if (low > high)
return -1;
  else if (naNums[guess] == nTarget)
  return guess;
  
  else if (naNums[guess] > nTarget )
 return binarySearch(naNums,nTarget,low,guess-1);
  
  else 
 return binarySearch(naNums,nTarget,guess+1,high);

}
2. Finish the the two binarySearch methods. The two argument version should use a loop, and the four argument version should use recursion. The correct output should be:    
`-1, 0, 1, -1, 4, -1`      
`-1, 0, 1, -1, 4, -1`    
Make sure you can find 3 & 10!    
3. Submit your finished pde file in to Google Classroom for the assignment
