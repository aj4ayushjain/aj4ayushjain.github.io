---
layout: post
title:  "DumbCoder Sort an set of Number ocurring in duplicates in array"
date:   2020-04-26 22:22:51 +0000
categories: [thought process,Interview Process,Gyan]  
---

Hello geniuses!

So, just today i finished up with an interview and realized how bad I am as a 
Problem Solver once again.But nothing is gonna stop me and i am soon gonna 
become RED!
Because dumb people too can make it big......Hhahahaha.



I will only focus on the Coding problem for now.

So the problem given to me was a Standard Problem 
	
	**Sort the array consisting of 0s, 1s & 2s** 

So I heard and solved it on leetcode before and had a idea insistenly to Use 
2/3 pointers approach.Now the interviewer asked me to code the solution.
So I began coding without any algortihm and thought process and after some time
came with a code and a bunch of changes which is exactly as it looks like I 
just copied from collabedit.

{% highlight java %}
we have an array of numbers which contains only 0s,1s and 2s

class z{
public static void main(String[] args){

    int sorted_arr = funct(arr);
}
public static int[] func(int[] arr){

int i=0;
int j=arr.length-1;

k=0;

// 0 , 0, 1, 1, 1 ,1 ,1,1,2,2,2,2,2,2
          |           |     |
          i            k     j
                  
while(k<=j){	<---change  dryrun
    
    while(arr[i]==0)    {
        i++;
        k++;
    }
    while(arr[j]==2)    j--;
       
    if(arr[k]==2){
        swap(k,j);
        j--;
        k++;
        k=i;	<-----change dryrun
    }
    if(arr[k]==1){
        k++;
    
    }
    if(arr[k]==0){
        swap(i,j);
        k++;
        i++;
        k=i;
    }
  
}
  
}
}
{% endhighlight %} 


So after writing while dry run too i made a few changes too.
So while somebody watched my code why i couldn't think and write in a few mins
time knowing the question before hand too.

The reasons
	1.) **Dry run in my mind before of approach** before you jump in code.
	2.) Write the **algorithm in steps before hand**. 

So the interviewer went on to ask a follow up on 
	-> What if there is 0s,1s,2s,3s what can be done
	-> And if there are 0s,1s,....ns dicuss upon a scalable approach he
           asked

So that point i thought for around a 30 sec and was quite a blank and told i 
don't know .

My mistakes 
	1.) Take more time and use pen and paper.
	2.) Make Use some todo checklist 

Then he told me about Counting Sort and at that moment I told i don't have idea
about that and asked is it similar to Bucket/Radix Sort and moved on.

So immediately after the interview without any google search I thought of it 
		**Counting Sort**
I think I got the correct answer then just after 2 mins don't know why I 
couldn't think of that time

So i guess it's like u 
	
{%highlight java%}
	1.)
	LinkedHashMAp
	 or
	HashMap/Array		Counter
	[n1]			  c1++;
	[n2]			  c2++;
	[n3]			  c3++;
	[n4]			  c4++; and so 	
	
	2.) Copy Array
	
	    c1 times    c2 times  c3 times  c4 times
	 -------------	-------- ---------- --------

		n1        n2         n3        n4
		
	 
{%endhighlight %}		

Time Comp - O(n)
Space Comp - O(n)


Updated Solution-Code and analysis of Mistakes

