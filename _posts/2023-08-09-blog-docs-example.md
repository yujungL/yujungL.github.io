---
layout: post
title: 작성 예시
tags: [docs]
categories: docs
---

일반 글 작성 **강조** 이모티콘 사용 가능[^1] 🐼

# 제목1
## 제목2
### 제목3
#### 제목4
##### 제목5
###### 제목6

[하이퍼링크는 이렇게](https://yujungl.github.io/)
### [하이퍼링크 제목도 가능](https://yujungl.github.io/)

## 표 작성

| hex | dec | oct |
| -   | -   | -   |
| 0   | 0   | 0   |
| 5   | 5   | 5   |

## 본문 주석
[^1]: 주석 1
{% include citation.html key="ref1" %}

## 삽입
> Suspendisse lectus leo, consectetur in tempor sit amet, placerat quis neque

## 이미지
{% include aligner.html images="/cake.jpeg" column=1 %}

## 목록
* 목록1
- list 1
    1. 숫자목록
    2. 숫자목록2
- list 2
  - sublist 1
    - subsub
      - subsubsub
        - subsubsubsub...
  - sublist 2
* 목록2
* 목록3

## 펼침
<details>
    <summary>누르시오</summary>
    펼쳐짐
</details>

## 수학
$$ f(x) = \int \frac{2x^2+4x+6}{x-2} $$

```markdown
$$ f(x) = \int \frac{2x^2+4x+6}{x-2} $$
```

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

## 코드 하이라이트
코드 올릴 때 사용

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

### Javascript
```javascript
/**
 * Does a thing
 */
function helloWorld(param1, param2) {
    const example = `hello ${param1}`
    var something = {
        key: "value",
        number: 1
    };

    // Do something
    if (2.0 % 2 == something) {
        console.log('Hello, world!');
    } else {
        return null;
    }

    // TODO comment
}
```

### JSON
```json
{
  "animals": {
    "tiger": {
      "name": "tiger",
      "images": ["🐯", "🐅", "⻁"]
    },
    "turtle": {
      "age": 126,
      "image": "🐢"
    },
    "unicorn": {
      "doesExist": true,
      "image": "🦄"
    }
  }
}
```

### html
```html
<!-- To generate a diagram -->
<div class="mermaid">
sequenceDiagram
    Alice->>John: Hello John, how are you?
    John-->>Alice: Great!
</div>
```

### XML
```xml
<part number="1976">
  <name>Windscreen Wiper</name>
  <description>The Windscreen wiper
    automatically removes rain
    from your windscreen, if it
    should happen to splash there.
    It has a rubber <ref part="1977">blade</ref>
    which can be ordered separately
    if you need to replace it.
  </description>
</part>
```

## bash
```bash
sed -i 's/\"hostname\"\:.*$/\"hostname\"\: \"'$IPADDR'\"\,/g' open-falcon/agent/config/cfg.json
```

## python
```python
#!/usr/bin/env python
"""
Test file for syntax
"""
```

### YAML
```yml

# Welcome to Jekyll!
#
# This config file is meant for settings that affect your whole blog, values
# which you are expected to set up once and rarely edit after that. If you find
# yourself editing this file very often, consider using Jekyll's data files
# feature for the data you need to update frequently.
#
# This file, "_config.yml" is *NOT* reloaded automatically when you use
# 'bundle exec jekyll serve'. If you change this file, please restart the server process.

# Site settings
# These are used to personalize your new site. If you look in the HTML files,
# you will see them accessed via {{ site.title }}, {{ site.email }}, and so on.
# You can create any custom variable you would like, and they will be accessible
# in the templates via {{ site.myvariable }}.

# SITE CONFIGURATION
baseurl: "/Type-on-Strap"
url: "https://sylhare.github.io"

# THEME-SPECIFIC CONFIGURATION
title: Type on Strap                                    # site's title
description: "A website with blog posts and pages"      # used by search engines
avatar: assets/img/triangle.png                         # Empty for no avatar in navbar
favicon: assets/favicon.ico                             # Icon displayed in the tab

remote_theme: sylhare/Type-on-Strap                     # If using as a remote_theme in github
```
