## 1.两数之和

用unordered_map<int, int>来记录前面出现过的元素以减少不必要的重复查找；把前面出现过的元素记录下来就行了，没必要多余的二次查找
用target减去当前值，再去hashmap中查找是否有这个差值，若存在则返回结果
hashMap插入键值对的两种方法：
1.下标操作符
hashMap[nums[i]] = i;
2.insert
hashMap.insert({nums[i], i});其中{nums[i], i}表示一个键值对
