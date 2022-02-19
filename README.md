# c#--fundamental

using System; <br>
using System.Linq; //array max,min etc built in  <br>
using System.Collections; // normal ds (stack,queue etc) <br>
using System.Collections.Generic; //generic ds (stack, queue etc with specific data type) <br>

public class Test
{
	public static void Main()
	{
		
    // int a = Convert.ToInt32(Console.ReadLine());
    // int b = Convert.ToInt32(Console.ReadLine());
    // Console.WriteLine(Math.Min('a','b'));
	// Console.WriteLine(Math.Floor(64.895));
	// Console.WriteLine(Math.Sqrt(64));
	 
	// char a = 'a';
	// Console.WriteLine('a');
	// Console.WriteLine(a);
	// string s = "abcdddd";
	// Console.WriteLine(s.Length);
	// s = s.ToUpper();
	// Console.WriteLine(s);
	// Console.WriteLine(s.IndexOf("c"));
	// Console.WriteLine(s.Substring(s.IndexOf("c")));

	// int[] num = {1,2,3,4,5};
	// for(int i=0;i<num.Length;i++) Console.WriteLine(num[i]);
	
	// string[] s = {"abcd", "df"};
	// for(int i=0;i<s.Length;i++) {
	// 	for(int j=0;j<s[i].Length;j++) Console.WriteLine(s[i][j]);
	// }
	
	// for each
	// string[] s = {"abcd", "df"};
	// foreach(string chunk in s) {
	// 	Console.WriteLine(chunk);
	// }
	
	
	// Sort a string
    // string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
	// Array.Sort(cars);
	// foreach (string i in cars)
	// {
	// 	 Console.WriteLine(i);
	// }
	

	// Sort Number
	// int[] myNumbers = {5, 1, 8, 9};
	// Array.Sort(myNumbers);
	// foreach (int i in myNumbers)
	// {
	// 	Console.WriteLine(i);
	// }
	
	
	// Uses System.Linq
	// int[] myNumbers = {5, 1, 8, 9};
    // Console.WriteLine(myNumbers.Max());  // returns the largest value
    // Console.WriteLine(myNumbers.Min());  // returns the smallest value
    // Console.WriteLine(myNumbers.Sum());  // returns the sum of elements
	
	
	// checkFunc(cars);
	
	// checkStack();
	
    // checkQueue();
    
    // checkList();
    
    // checkMap();
	
	
	}
	
	static void checkFunc(string[] s){
		for(int i=0;i<s.Length;i++) {
			Console.WriteLine(s[i]);
		}
	}
	
	static void checkStack(){
		Stack q = new Stack();
		q.Push(1);
		q.Push(2);
		q.Push(3);
		Console.WriteLine(q.Count);
		foreach(int i in q){
			Console.WriteLine(i);
		}
		
		//generic
		Stack<char> q2 = new Stack<char>();
		q2.Push('a');
		q2.Push('b');
		q2.Push('c');
		Console.WriteLine(q2.Count);
		foreach(int i in q2){
			Console.WriteLine((char)i);
		}
	
	}
	
	static void checkQueue(){
		Queue q = new Queue();
		q.Enqueue(1);
		q.Enqueue(2);
		q.Enqueue(3);
		Console.WriteLine(q.Count);
		foreach(int i in q){
			Console.WriteLine(i);
		}
		
		//generic
		Queue<char> q2 = new Queue<char>();
		q2.Enqueue('a');
		q2.Enqueue('b');
		q2.Enqueue('c');
		Console.WriteLine(q2.Count);
		foreach(int i in q2){
			Console.WriteLine((char)i);
		}
	
	}
	
	static void checkList(){
		List<int> numbers = new List<int>() { 1, 2, 5, 7, 8, 10 };
		numbers.Add(13);

		Console.WriteLine(numbers[3]); // prints 7

		// using foreach LINQ method
		numbers.ForEach(num => Console.WriteLine(num + ", "));

		// using for loop
		for(int i = 0; i < numbers.Count; i++) Console.WriteLine(numbers[i]);
			
	}
	
	static void checkMap(){
		var map = new Dictionary<string, int>();
		map.Add("farhan", 25);
		map.Add("abcde", 1);
		Console.WriteLine(map["farhan"]);
		
		foreach(var mp in map){
			Console.WriteLine(mp.Key + " = " + mp.Value);
		}
	}
}
