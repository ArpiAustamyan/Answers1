## Questions - Answers ##
1. ##### What teams at Vineti are you interested in and why? (Dev or QA)#####
I am interested in Software Development , because every day we solve new tasks ,we acquire new knowledges ,we are facing with various problems and  try to overcome them .Software developer  Technology is extremely fast moving ,so  I need to be able to learn new programming languages . I like also that it requires team work ,communication skills.

2. ##### What is your favorite programming language and why? #####
My favorite programming language is c++ .I started learning programming from c++ .It helps me to learn new programming languages ,because basic principles are the same in OOP programming languages.

3. ##### What is a linked list? #####
Linked list is linear collection of elements (nodes). Each node consists of data and the reference to the next node of the list.
The first node of list is head.	The last node has a reference to null.
The advantage of linked list over array is, that linked list allows insertion and removal of nodes at any point in the list. One of disadvantages linked list is that they use more memory than arrays because of the storage used by their pointers. Linked list does not have any form of efficient indexing and for that reason is difficult to find element is list.

4. ##### You work in an ice cream shop and step into the back for a few minutes. You return and see a large group of people waiting. How would you serve them? #####
  I will give the ice-cream to those who have spent more time to for waiting.
  
5. ##### How would you test a pen? #####
	At first, I will write to test if a pen is writing and if it is I will test on which surfaces it can write and we can also test with what color it is written.

6. ##### As a test engineer in Amazon what would you test first (assuming authentication functionality is already covered)? #####
I will test components of a project.  My work will include  writing tests,building testing infrastructure, collecting and reporting on testing metrics, participating in product design meetings etc. I need the skills like  strong coding, design and analytic thinking .

7. ##### You have a list of numbers from one to one million and there is a missing number. How would you find the missing number? #####
	At first, I will get the sum of list members  and after subtracting from the sum of one to one million numbers
  ``` c++
  int  MissingNumber (int* arr, int n)
{
    int sum = 0;
    int nsum = (n+1) * (n+2) / 2;
    for(int i=0 ;i<n ;i++)
    {
        sum += arr[i];
    }
    return nsum - sum;
}
```

8. ##### How would you determine the angle between the hour-hand and minute-hand of a clock at 3:20? #####
The numbers of the clock divide the circle into 12 equal sectors. The angle between 3 and 4 numbers is  equal to 30(360/12=30) .Since it is 3:20 at a clock ,hour-hand has already passed one third (20/60=1/3) of the  angle .So the angle between the hour-hand and minute-hand of a clock at 3:20 is equal to 20 ( 30-(30/3)=20).
9. ##### How would you determine if a number is a power of two?

``` c++
bool PowerTwo (int n)
{
    int m = n-1;
    return !(n & m);  
}
```
10. ##### How would you remove duplicates from a list? #####

``` c++
void Remove(int num[], int index, int &size)
{
	int i;
	for (i = index; i < size - 1; i++)
		num[i] = num[i + 1];
	size--;
}

void removeDuplicate(int num[], int &size)
{
	int i, j;
	int numb;
	for (i = 0; i < size; i++)
	{
		numb = num[i];
		for (j = i + 1; j < size; j++)
		{
			if (numb == num[j])
			{
				Remove(num, j, size); j--;
			}
		}
	}
}

```
11. ##### How would you determine if a string has all unique characters? #####
``` c++
bool IsUnique(string s)
{
	for (int i = 0; i < s.length(); i++)
		for (int j = i + 1; j < s.length(); j++)
			if (s[i] == s[j])
				return false;
	return true;
}
```

12. ##### How would you reverse a string? #####
``` c++
void Reverse(string& Str)
{
	char c;
	for (int i = 0; i < Str.size() / 2; i++)
	{
		c = Str[i];
		Str[i] = Str[Str.size() - i - 1];
		Str[Str.size() - i - 1] = c;
	}
}
```
13. ##### How would you compress a string such that 'AAABCCDDDD' becomes 'A3BC2D4'? Only compress the string if it saves space. #####
``` c++
void Compress(string& Str)
{
	string newS;
	char c;
	int i = 0;
	int j = 0;
	while (i < Str.size())
	{
		j = 0;
		c = Str[i];
		newS += Str[i];
		while (c == Str[i])
		{
			j++;
			i++;
		}
		if (j != 1)
			newS += j+'0';
	}
	Str = newS;
}
```

14. ##### Given an array of 0's and 1's, how would you move all of the 0's to the beginning of the array and all of the 1's to the end of the array? #####
``` c++
void sortArray(int* arr,int n)
{

    int i=0, j=n-1;
    while(i!=j)
    {
        if(arr[i]==1 && arr[j]==0)
          {
              arr[i]=0;
              arr[j]=1;
              i++;j--;
            }
        else
        {
            if(arr[i]==0)
            i++;
            if(arr[j]==1)
            j--;
        }
    }
}
```
15. ##### How would you design a vending machine or a toaster? #####
First I have to know what amount of money I need to design toaster.I need to know the size of the toaster.I will get the answers of this questions
How does it work? Is it timer based or manual toaster?
How many years of guarantee it has?
How much power limit does it operate ?

16. ##### You have two lightbulbs at a 100-story building. You want to find the lowest floor at which the bulbs will break when dropped. How would you find the floor using the least number of drops? #####
First lightbulb we  drop from 16-th floor .If it breaks ,we will search the floor between 1 and 16 .So in the worst case we drop 16 times . If we drop the lightbulb from 16-rd floor and it does not break we drop it from 31-stfloor(16+15).If it breaks ,we will search the floor between 17 and 31.Since we have  already dropped the bulb from 16rd floor ,the count of the throws in the worst case is equal to 16 (15+1).If it does not break we will drop it from 45-th(16+15+14)floor. If it breaks ,we will search the floor between 31 and 45 .Since we have  already dropped the bulb from 16th and 31-st
 floors ,the count of the throws in the worst case is equal to 16 (14+1+1).Then we continue this process dropping  it from 58-th,70-th,81-st,91-st,100 floors .In any Case the maximum count of throwing is equal to 16.
17. ##### If you have a square room with no roof, and you had four pillars you had to plant on the walls so that each pillar touched two walls, how would you do it? #####
I denote with y*sqrt(2) the side of roof square.
In the roof square I   put  a square which is consisted of pillars (the length of the sides of this square are equal to y).The peaks of this square are the midpoints of the roof square sides .So we have a square on the walls of room ,which is embraced in the roof square and its each side touches two walls.

18. ##### Given 9 balls all of which weigh the same except for one, what is the minimum of weightings necessary to find the ball weighs more (or less)? #####
For convenience I denote with X he ball weigh  of which is not equal to weight of others..
I will divide them into 3 parts . Each part is consisted  of 3 balls . lets denote this parts by numbers 1,2,3. Then  I will weigh 1 and 2 .
Here can occur 2 cases.      
Case A

1)If their weights are equal , X  is in the 3rd part.
 2)I will weight second and third parts to know  whether the weight of X is more or less than others .
3)Then I will weight any two balls of 3rd part  .The X is The ball which has more (less) (it is connected with previous step) weight than others .

Case B

1)If the weight of the first part is more(less) than the weight of the second part

2)I will weight  the first(second) and third parts.

3) If their weights are equal ,  X is in the second(first )part and its weight is less (more ) than others weight( it is connected with the previous step).Then I will weight any 2 balls of the second ( first) part .X is the ball which weight is less (more) than others.

4) If the weight of the  first(second) part is more than the third parts weight ,X is in the first(second) part and the weight of X is more (less) than others weight .Then I will weight any 2 balls of the first part .X is the ball which weight more (less)than the weight of others.
So we can solve this problem with minimum 3 weightings.
19. ##### How would you solve the N Queens problem? [Bonus] #####
20. ##### How would you find the longest palindrome in a string? [Bonus] #####
