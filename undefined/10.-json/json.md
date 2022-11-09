# 💒 JSON 이해에 필요한 기본 개념

## **💡**HTTP (HyperText Transfer Protocol)

* 브라우저와 서버간 데이터 (링크, 텍스트, 이미지 등) 통신 규약&#x20;
* 데이터 요청, 서버는 그에 맞는 응답&#x20;
* HyperText - 전반적으로 쓰여지고 있는 리소스(문서, 이미지파일 등)

## **💡**AJAX (Asynchronous Javascript And XML)

* 전체 페이지 새로고침 않고도 일부 데이터 전송 가능.

## **💡**XHR (XMLHttpRequest)

* 브라우저 API중 하나.
* AJAX에서 데이터 교환할 때 사용하는 Object

## **💡**fetch() API : 데이터 교환 위해 최근 등장. (IE는 지원 X)

## **💡**XML (Extensible Markup Language)

* 데이터 전송에 유리하도록 확장된 마크업 언어&#x20;
* 태그명 자유롭게 명명 가능. 요즘 많이 사용하지 않음



{% hint style="info" %}
※ 전송 데이터 형태 : XML・JSON&#x20;

※ 데이터 전송 방법 : XMLHttpRequest ・ fetch() 이용해 서버와 통신.
{% endhint %}



## **💡💡**JSON (JavaScript Object Notation)**💡** **💡**

* JS 객체 명세서.  데이터를 저장・교환할 때 유용. (ECMAScript 3rd 1999)&#x20;
* 모바일에서 서버와 데이터를 주고 받을때, 서버와 통신을 하지 않아도 오브젝트를 시스템에 저장할 때 사용

{% tabs %}
{% tab title="object 형태" %}
{key:value, key:value, ...}
{% endtab %}

{% tab title="json 형태" %}
{"key":"value", "key":"value",...}
{% endtab %}
{% endtabs %}



## **💡**JSON 특징

1. 가장 간단한 데이터 교환 포맷.
2. 가벼운 텍스트 기반 구조.
3. 읽기 편함. (Easy to read)
4. 이름:값 형식. (Key:value pairs)
5. 데이터 전송에 편리한 형식으로 저장 (= 직렬화)하는데 사용.
6. 독립적인 프로그램 언어・플랫폼
