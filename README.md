1.Task:-
Find the missing number in a sequence of numbers.?
Input: nums = [4,1,5,3,6] 
Output: 2

Program of this Task,

package package3;



public class MissingNumber {



    public static int getMissingNo(int[] arr, int n)

    {

        int M = n+1;

        int totalSum = M * (M + 1) / 2;



        int arraySum = 0;

        for (int num : arr) {

            arraySum += num;

        }



        return totalSum - arraySum;

    }



    public static void main(String[] args)

    {

        int[] arr = {4,1,5,3,6};

        int M = arr.length;

        System.out.println(getMissingNo(arr, M));

    }

}



================================================================================================================



2.Task:-

Given a string s, find the first non-repeating character in it and return its index. If it does not exist, return -1.
	Input: s = "loveleetcode"
	Output: 2



Program of this Task,



package package3;



import java.util.HashMap;

import java.util.Map;



public class FirstUniqueCharacter {

    public static int firstUniqCharUsingMap(String s) {

        Map<Character, Integer> charCount = new HashMap<>();

        

        for (char c : s.toCharArray()) {

            charCount.put(c, charCount.getOrDefault(c, 0) + 1);

        }

                for (int i = 0; i < s.length(); i++) {

            if (charCount.get(s.charAt(i)) == 1) {

                return i;

            }

        }

        

        return -1;

    }



    public static void main(String[] args) {

        String s = "loveleetcode";

        System.out.println(firstUniqCharUsingMap(s));

    }

}

===========================================================================
