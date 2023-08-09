---
layout: post
title: 작성 예시
tags: [docs]
categories: docs
---

일반 글 작성 **강조** 이모티콘 사용 가능 🐼

# 제목1
## 제목2
### 제목3
#### 제목4
##### 제목5
###### 제목6

[하이퍼링크는 이렇게](https://yujungl.github.io/)
### [하이퍼링크 제목도 가능](https://yujungl.github.io/)

## 코드 하이라이트
코드 올릴 때 사용

## python
```python
#!/usr/bin/env python
"""
Test file for syntax
"""
```

## java
```java
@SuppressWarnings("unchecked")
@RequestMapping(value = "/customerHelp/findErpHoliday")
public void findErpHoliday(HttpServletRequest request, HttpServletResponse response) throws Exception {
    JSONObject obj = new JSONObject();

    //국경일외에 DB에서 배송 제외일 조회
    org.json.JSONArray list = customerService.selectExceptDay(request); 	// 추후 배송DB 확인해서 넣기
    try {
        obj.put("data", list);
    } catch (Exception e) {
        e.toString();
    }finally{
        response.getWriter().write(obj.toJSONString());
    }

}
```

## 표 작성

| hex | dec | oct |
| -   | -   | -   |
| 0   | 0   | 0   |
| 5   | 5   | 5   |


## KaTeX

Some KaTeX diagrams to check in dark mode:

$$
\begin{CD}
A @>a>> B \\
@VbVV @AAcA \\
C @= D
\end{CD}
$$

$$\utilde{AB}$$

## Mermaid

<div class="mermaid">
flowchart TB
    c1-->a2
    subgraph one
    a1-->a2
    end
    subgraph two
    b1-->b2
    end
    subgraph three
    c1-->c2
    end
</div>

