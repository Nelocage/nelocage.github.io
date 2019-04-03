## reverse函数：反转容器内容

reverse函数可以反转一个容器中的内容，包含在<algorithm>库中。

==1、函数原型==

reverse函数等同于下面的代码：

```c++
template <class BidirectionalIterator> void reverse (BidirectionalIterator first, BidirectionalIterator last)
{
     while ((first!=last)&&(first!=--last))
     {
          std::iter_swap (first,last);
          ++first;
     }
}
```



reverse函数使用iter_swap来交换两个元素。
==2、参数：first、last==

first和last是**双向迭代器类型**，reverse函数反转的范围是[first,last)，所以包括first指向的元素，不包括last指向的元素。

==3、返回值==

reverse函数没有返回值。

==4、例子==

```c++
// reverse algorithm example
#include <iostream>    
// std::cout
#include <algorithm>   
// std::reverse
#include <vector>      
// std::vector
 
int main () {
    std::vector<int> myvector;
    // set some values:
    for (int i=1; i<10; ++i) myvector.push_back(i);   // 1 2 3 4 5 6 7 8 9
    std::reverse(myvector.begin(),myvector.end());    // 9 8 7 6 5 4 3 2 1
    // print out content:
    std::cout << "myvector contains:";
    for (std::vector<int>::iterator it=myvector.begin(); it!=myvector.end(); ++it)
        std::cout << ' ' << *it;
    std::cout << '\n';
    return 0;
}
```



输出：
myvector contains: 9 8 7 6 5 4 3 2 1
==5、复杂度==

循环交换首尾元素。因此复杂度是线性的，并且循环半个数组长度。

vector实现反转：

```c++
reverse(vector.begin(), vector.end());
```

输入一个链表，从尾到头打印链表每个节点的值：

```c++
//第一种方法
#include <iostream>
#include <vector>
using namespace std;
struct ListNode
{
    int val;
    struct ListNode* next;
    ListNode(int x)
    : val(x), next(NULL)
    {
    } 
};
 
class Solution
{
public:
    vector<int> printListFromTailToHead(ListNode* head)
    {
        ListNode* p = head;
        vector<int> tmp;
        
        while(head!=NULL)
        {
            tmp.push_back(head->val);  //每次都插到尾部
            head = head->next;
        }
        
        reverse(tmp.begin(), tmp.end());   //一句话实现vector反转
        
        return tmp;
    }
};

//第二种方法
class Solution
{
public:
	vector<int> printListFromTailToHead(ListNode* head)
	{
		ListNode* p = head;
		vector<int> tmp;
		
		while(head!=NULL)
		{
			tmp.insert(tmp.begin(), head->val);  //每次插到vector头部，这样不用反转
			head = head->next;
		}
		
		return tmp;
	}
};

```

## unorder_map的使用方法

<https://www.sczyh30.com/posts/C-C/cpp-stl-hashmap/>

## C++pair用法

<https://blog.csdn.net/sinat_35121480/article/details/54728594>

## C++ map

<https://blog.csdn.net/shuzfan/article/details/53115922>

## C++ vector

vector的一些注意事项<https://blog.csdn.net/shuzfan/article/details/72784259>