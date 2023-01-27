## Lab Report 3
**Part 1**
![code](https://user-images.githubusercontent.com/73797155/215192527-47bbbadf-0aa6-4c56-a581-9e925878e77d.PNG)  

![serverss1](https://user-images.githubusercontent.com/73797155/215192533-aaaa2b33-3f48-4730-835e-96539bf65159.PNG)  
The `handleRequest` method is called.
`s` starts as an empty string.  
`url` is localhost:4000/add-message?s=have a nice day!!!  
`url.getPath()` is \add-message  
`message` is "have a nice day!"  
`message` is added to `s` which is now "have a nice day!!!"  
And s is printed

![serverss2](https://user-images.githubusercontent.com/73797155/215192538-73925d84-c72f-4d27-a2de-e88147bb8464.PNG)  
`s` starts as "have a nice day!!!".  
`url` is localhost:4000/add-message?s=and this is another message
`url.getPath()` is \add-message  
`message` is "and this is another message"  
`message` is added to `s` which is now 
```
have a nice day!!!
and this is another message
```
And s is printed  
  
**Part 2**

```
@Test
public void testAverageWithMultipleLowest(){
  double[] input2 = {1.0, 1.0, 2.0, 3.0};
  double avg = ArrayExamples.averageWithoutLowest(input2);
  assertEquals(2.0, avg, 0);
}

@Test
public void testAverageWithUniqueLowest(){
  double[] input2 = {1.0, 2.0, 3.0};
  double avg = ArrayExamples.averageWithoutLowest(input2);
  assertEquals(2.5, avg, 0);
}
```
![image](https://user-images.githubusercontent.com/73797155/215193884-db3fc68c-9d96-487d-8328-e7bc5d361961.png)

Before:  
```
static double averageWithoutLowest(double[] arr) {
  if(arr.length < 2) { return 0.0; }
  double lowest = arr[0];
  for(double num: arr) {
    if(num < lowest) { lowest = num; }
  }
  double sum = 0;
  for(double num: arr) {
    if(num != lowest) { sum += num; }
  }
  return sum / (arr.length - 1);
}
```

Fixed:  
```
static double averageWithoutLowest(double[] arr) {
  if(arr.length < 2) { return 0.0; }
  double lowest = arr[0];
  double sum = 0;
  for(double num: arr) {
    if(num < lowest) { lowest = num; }
    sum += num;
  }
  return (sum-lowest) / (arr.length - 1);
}
```

This fixes the issue that the lowest value in the array is not unique, it subtracts out all of the lowest values.
Now, only 1 instance of the lowest value is subtracted, which is the intended behavior.
  
**Part 3**
I learned about how to create and execute different JUnit tests, as well as the terminology necessary to accurately describe any issues I am facing.
I was not aware of the diference between symptoms, faliure-inducing inputs, and bugs before. It was also interesting to see how these JUnit tests could
be used to help me with debugging, and some of the methodology in thouroughly finding bugs in my code.
