# LeetCode-75-Merge-Strings-Alternately-answer
LeetCode 75 Merge Strings Alternately answer in c++

You are given two strings word1 and word2. Merge the strings by adding letters in alternating order, starting with word1. If a string is longer than the other, append the additional letters onto the end of the merged string.

Return the merged string.

 

Example 1:

Input: word1 = "abc", word2 = "pqr"
Output: "apbqcr"
Explanation: The merged string will be merged as so:
word1:  a   b   c
word2:    p   q   r
merged: a p b q c r
Example 2:

Input: word1 = "ab", word2 = "pqrs"
Output: "apbqrs"
Explanation: Notice that as word2 is longer, "rs" is appended to the end.
word1:  a   b 
word2:    p   q   r   s
merged: a p b q   r   s
Example 3:

Input: word1 = "abcd", word2 = "pq"
Output: "apbqcd"
Explanation: Notice that as word1 is longer, "cd" is appended to the end.
word1:  a   b   c   d
word2:    p   q 
merged: a p b q c   d
 

Constraints:

1 <= word1.length, word2.length <= 100
word1 and word2 consist of lowercase English letters.












solution:
class Solution {
public:
    string mergeAlternately(string word1, string word2) {
        int m=word1.size(),n=word2.size();
        string ans;
        for(int i=0;i<m||i<n;i++){
        if(i<m)ans += word1[i];
        if(i<n)ans += word2[i];
        }
        return ans;
    }
};
