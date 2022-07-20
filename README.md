ASS1:METHOD 1:
class Solution:
    def reverseString(self, s: List[str]) -> None:
        for i in range(len(s)//2):
            s[i],s[-i-1]=s[-i-1],s[i]
        return s
        
METHOD 2:
class Solution:
    def reverseString(self, s: List[str]) -> None:
        def reverse(left,right,l):
            if left > right:
                return
            s[left], s[right] = s[right], s[left]
            reverse(left+1, right-1,s)
        reverse(left=0,right=len(s)-1,l=s)
