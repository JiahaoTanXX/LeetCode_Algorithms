## 1.两数之和
用unordered_map<int, int>来记录前面出现过的元素以减少不必要的重复查找；把前面出现过的元素记录下来就行了，没必要多余的二次查找
用target减去当前值，再去hashmap中查找是否有这个差值，若存在则返回结果
hashMap插入键值对的两种方法：
1.下标操作符
hashMap[nums[i]] = i;
2.insert
hashMap.insert({nums[i], i});其中{nums[i], i}表示一个键值对

## 49.字母异位词分组
同理，使用hashMap进行处理，第一个键值为字符串标识符，第二个键值为字母异位词组；
Tip：因为sort会直接改变字符串的值，所以我们开一个新的字符串key来帮助我们标记相同字母异位词
sort的用法：sort(key.begin(), key.end());
最后在应用autol类型来将分类后的字母异位词分组插入ans
eg：for(auto it : hashmap) 

## 128.最长连续序列
key point：为了减少重复的查找，我们需要判断某数字是否是序列的开始；当找到序列的开头数字时即可用while进行查找
我们只需要知道一个数字是否存在，所以使用unordered_set
