# Find-the-Index-of-the-First-Occurrence-in-a-String
Given two strings needle and haystack, return the index of the first occurrence of needle in haystack, or -1 if needle is not part of haystack.

class Solution:
    def strStr(self, haystack, needle):
        if not needle:
            return 0

        haystack_len = len(haystack)
        needle_len = len(needle)

        for i in range(haystack_len - needle_len + 1):
            if haystack[i:i+needle_len] == needle:
                return i

        return -1


sol = Solution()

haystack1 = "sadbutsad"
needle1 = "sad"
print(sol.strStr(haystack1, needle1))  

haystack2 = "leetcode"
needle2 = "leeto"
print(sol.strStr(haystack2, needle2))  

