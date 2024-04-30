# 題目:
![image](https://github.com/HoChenYu/Leetcode-programing-practice/assets/63805851/8fe7efdd-b21e-4f66-9b8b-4fc9c654c6e6)
# 解題思路:
這題要找兩個字串中的最大公因數，因此如果str1和str2中存在某一個最大公因數時，str1+str2==str2+str1這個條件會成立  
利用三元運算子（Ternary Operator)```` a ? b : c````如果a條件符合執行b，不符合執行c  
利用substr()這個member function對str1進行字串的提取(初始位置,要提取的字串長度)  
````gcd(size(str1),size(str2))````由於前面a成立，接著只要找字串之間的長度的最大公因數即可  
# 程式碼:
````C++
class Solution {
public:
    string gcdOfStrings(string str1, string str2) {
        return (str1 + str2 == str2 + str1)? 
        str1.substr(0, gcd(size(str1),size(str2))): "";
    }
};
````
