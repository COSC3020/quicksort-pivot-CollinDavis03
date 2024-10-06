# Quicksort Pivots

in the lectures I only briefly mentioned strategies for determining a good pivot
for quicksort. The implementation on the slides simply picks the leftmost
element in the part of the array that we consider as a pivot. I also mentioned a
few other ways of picking a good pivot, e.g. randomly.

Median-of-three is also a good way of picking a pivot -- inspect the first,
middle, and last elements of the part of the array under consideration and
choose the median value. Using the probabilities for picking a pivot in a
particular part of the array (in the same way as we did on slide 34), argue
whether this method is more or less (or equally) likely to pick a good pivot
compared to simply choosing the first element. Assume that all permutations are
equally likely, i.e. the input array is ordered randomly.

Your answer must derive probabilities for choosing a good pivot and
quantitatively reason with them.

Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

Looking back at slide 34 in the slides provided to us in class. We know that there is a 1/2 chance of selecting a good pivot. The reason is that there is a chance that the picot will be larger or smaller than the good pivot selection if we use the median method of a 3-pivot method. It will choose the first, middle, and last elements of an array given. Out of those three elements, it will choose the median value. The only way this will not work is if all the values by some chance have the exact value. For it to be considered a good pivot, it will have to create two partitions, one being at most 3n/4. With this method, it will have a 1/2 chance of being a good pivot, With that logic we are going to create all the possibilities of arrays to get the value needed. S = smaller than good pivot, G = good pivot, M = More than good pivot. 

The possible arrays following the three array method: 
(SSS), (SSG), (SSM), (SGG), (SGM), (SGS), (SMS), (SMM), (SMG), (GGG), (GGS), 
(GGM), (GSM), (GMS), (GSS), (GMM), (GMG), (GSG), (MMM), (MMS), (MMG), (MSS), 
(MGG), (MSG), (MGS), (MSM), (MGM)

The median value is in between the others. It will not be the smallest or the largest:
1(SSS), 3(SSG), 3(SSM), 3(SGG), 6(SGM), 3(SMM), 1(GGG), 3(GGM), 3(GMM), 1(MMM)

With that the permutations will also be different so G = 1/2, S = 1/4, and M = 1/4. The reason for the 1/4 is because the 3 method will choose good(x) or bad(Y) pivots. With this, the probability will be:

1*(SSS) = p\ (1/4)^3 p = 1/64
Y 3*(SSG) =  (1/4)^2 ∗1/2 = 1/32 = 2/64 x 3 = 6/64 
Y 3*(SSM) = p\ (1/4)^3 p = 1/64 x 3 = 3/64 
Y 3*(SGG) = p\ (1/4) * (1/2)^2 $ = 1/16 = 4/64 x 3 = 12/64
X 6*(SGM) = (1/4)^2 ∗ 1/2 = 1/32 = 2/64 x 6 = 12/64 
X 3*(SMM) = p\ (1/4)^3 $ = 1/64 x 3 = 3/64 
Y 1*(GGG) = p\ (1/2)^3 $ = 1/8 = 8/64 
X (GGM) = p\ (1/4) * (1/2)^2 $ = 1/16 = 4/64 x 3 = 12/64
X 3*(GMM) =  (1/4)^2 ∗ 1/2= 1/32 = 2/64 x 3 = 6/64
Y 1*(MMM) = p\ (1/4)^3 $ = 1/64

The good pivots are 44/64 or (11/16), and the bad pivots are 20/64 or (5/16). 

With using the median method the result for good pivots is 11/16 or 69% of the time. Which is significantly higher than the 50% chance we had at the start. With all of that, the median of the 3 methods has a better chance of choosing a good pivot than compared to the first element. 

Sources: 
I did the majority of this on Google Docs and had to copy it over from what I had. I also looked at Nolan's quicksort pivot to make sure I had the right final answer and I was moving in the right direction with the assignment. The only other thing I used was Google and ChatGPT to try to get the exponents to look like exponets but that did not work out very well for me. 

Plagiarism Statement: 
“I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.”


