---
date: '2023-09-19'
title: Temp titlen temp title temp title temp title temp title temp title temp title
tags: [temp2, temp3]
author: viraj
description: dummy description 
---

Sherlock Holmes

```java

class Solution {
    public int minDeletions(String s) {
        int[] count = new int[26];
        for(char c : s.toCharArray()){
            count[c - 'a']++;
        }
        
        PriorityQueue<Integer> pq = new PriorityQueue<>(Collections.reverseOrder());
        for(int i: count){
            if(i != 0)
                pq.add(i);
        }
        
        int last = -1;
        int ans = 0;
        while(!pq.isEmpty()){
            
            if(last == -1){
                last = pq.poll();
                continue;
            }
            
            int current = pq.poll();
            
            if(current == 0)
                continue;
            
            if(last == current){
                pq.add(current - 1);
                ans++;
            }else{
                last = current;
            }
            
        }
        
        return ans;
    }
}


```

XXXX