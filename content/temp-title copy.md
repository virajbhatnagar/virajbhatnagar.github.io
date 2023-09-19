---
date: '2023-09-19'
title: Temp titlen temp title temp title temp title temp title temp title temp title
tags: [temp2, temp3]
link: https://twitter.com/Nithin0dha/status/1563133544884760576
author: viraj
description: dummy description jasd kasdhfk aKSDHj aSKcdnlA ZHDxkk ZKDXch laSNZDKXbkasd LZHDkashbdk
---

Sherlock Holmes & John Watson 2
The following is an example of a homepage template that uses partial, base templates, and a content file at content/_index.md to populate the {{ .Title }} and {{ .Content }} page variables.

The homepage of a website is often formatted differently than the other pages. For this reason, Hugo makes it easy for you to define your new site’s homepage as a unique template.
Homepage is a Page and therefore has all the page variables and site variables available for use.

The homepage template is the only required template for building a site and therefore useful when bootstrapping a new site and template. It is also the only required template if you are developing a single-page website.

https://www.github.com/zerodha/nithinkamath.me/blob/develop/layouts/_default/list.html

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