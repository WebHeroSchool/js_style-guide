# **JavaScript Style Guide**

### ++��� ������ ���� ����������� �������� � ��������.++
 ��� � ���� ��������� ���������������� � ����� ������� ������ � �������� ����� ��� ��� � �������, ������� � ��������� ��������, � ����� ��������, ������� ��� �����. ��� ����� ����� ������� ����� ��������� ����. 

**�� ���� ������� �� �������� ����� ������������**
*����� ��� �������� ������. ��� �������� ������������, � �� ����������� �����.* ;-)

---

***

## **1. �������� ������**
---
#### � ����������� JavaScript �������� �������� ������ ������� � ��� ���������� ����������� ����� � ����������� ������� �� ��� �� ������, ��� � ��������������� �������� ����� � �� �� ����� ������. ����� ����������� ������� ������ ���� ������, ��� �����:
``` js
if (condition) {
  // ����� ���
  // ...� ���
  // ...� ����� ���
}
``` 

## **2. ����� ������**
---
#### ����� �� ����� ������ ������� �������������� ������ ����. ����� ����� ��������� ��, ��������:
``` js
// �������� ������� ` ��������� ��������� ������ �� �����
let str = `
  ������� ������ TC39 ����������� Ecma International -
  ��� ������ JavaScript-�������������, ���������� � ������� ������� JavaScript,
  ������� ������ � ����������� ���������� ���������� � ��������� ����� JavaScript.
`;
``` 
��� ��� if:
``` js
if (
  id === 123 &&
  moonPhase === 'Waning Gibbous' &&
  zodiacSign === 'Libra'
) {
  letTheSorceryBegin();
}
``` 
������������ ����� ������ ������������� � �������. ������ ��� `80` ��� `120` ��������.

## **3. �������**
---
#### ���������� ��� ���� ��������:

**�������������� �������: ��� ��� ������ �������.**

�������������� ������ ����������� � ������� 2 ��� 4 ��������, ��� ������� ��������� (������� ==Tab==). ����� �� ��� ������� � ��� ��� �� ���� ����������. ������� ������ ��������������.

���� �� ����������� �������� ��� ���������� ����������� � ���, ��� ������� ��������� ����� ������ ������������ ��������, ��� ������ ���������.

��������, �� ����� ��������� ��������� ������������ ����������� ������:
``` js
show(parameters,
     aligned, // 5 �������� �����
     one,
     after,
     another
  ) {
  // ...
}
```
**������������ �������: ������ ������ ��� �������� ���� �� ����������� �����.**

���� ���� ������� ����� ����� ��������� �� ���������� �����. � ������� ���� ��������� ������������� ����������, �������� ���� � ������������ ���������:
``` js
function pow(x, n) {
  let result = 1;
  //              <--
  for (let i = 0; i < n; i++) {
    result *= x;
  }
  //              <--
  return result;
}
```
���������� �������������� ������� ������ ����, ��� ��� ������� ��� ����� ��������. �� ������ ���� ����� 9 ����� ���� ������ ��� ������������� �������.

## **4. ����� � �������**
---
#### *����� � ������� ������ �������������� ����� ������� ���������, ���� ���� ��, �������� ��, ����� ����������.*

���� �����, � ������� ����� � ������� ������������� � ����� ������������. ������ � JavaScript ������ ������, ����� ������� ������ �� ����������������, ��� ����� � �������, ��� ����� �������� � �������. ��������� �� ���� � � ����� � ��������� ����.

���� �� � ������� ����������� �� JavaScript, �� ����� ������� ����� ���� ��� ����� � �������, �������� StandardJS. � ���� ������, ����� ����� ������������ ����� � �������, ����� �������� ��������� ������. ����������� ������������� �� ������.

## **5. ������ �����������**
---
#### ������� ����������� ������ ���� �������.
��������, � ����� ������ ������� ������������ ��������� ==continue==, ����� �������� ������ �����������.
��������, ������ ���������� ���������� ������� ==if==, ��� �����:
``` js
for (let i = 0; i < 10; i++) {
  if (cond) {
    ... // <- ��� ���� ������� �����������
  }
}
```
�� ����� ��������:
``` js
for (let i = 0; i < 10; i++) {
  if (!cond) continue;
  ...  // <- ��� ������� ������ �����������
}
```
����������� �������� � � ==if/else== � ==return==.

## **6. ���������� �������**
---
#### ���� �� ������ ��������� ��������������� �������, � ����� ������������ ��� ���, �� ���������� ��� ������� ����������� �������.
*1. �������� ������� ����� �����, ������� �� �������:*
``` js
// ���������� �������
function createElement() {
  ...
}

function setHandler(elem) {
  ...
}

function walkAround() {
  ...
}

// ���, ������� ���������� ��
let elem = createElement();
setHandler(elem);
walkAround();
```

*2. ������� ���, ����� �������*
``` js
// ���, ������������ �������
let elem = createElement();
setHandler(elem);
walkAround();

// --- ��������������� ������� ---
function createElement() {
  ...
}

function setHandler(elem) {
  ...
}

function walkAround() {
  ...
}
```

*3. ��������� �����: ������� ����������� ���, ��� ��� ������������ �������.*

� ����������� ������� ������ ������� �������� ����������������.

��� ������, ��� ��� ������ ���� �� ������� ����� �����, *��� �� ������*. ���� ������� ��� ���, �� ��� ��� �� ���������� �������. � �����, ����� ����, ��� ������ �� ����� ����� ������ �������, �������� ���� �� ����� ������ ���������.

## **7. ����������� �������� ����� ���������� � �������**
---
��� ������� ����� ������, ����� ��� ��� ��������� ���������� ��������, ������������ ����� ������� � ����������. ��� �� ����� �������� ���:
``` js
function avg (a) {
	let s = a.reduce((x,y ) => x + y)
  return s / a.length
}
```
��� ������������� ����������� ���������, ���� ������������ � ��� �������� ����� ���������� � �������, ���������� �� �����.
``` js
function averageArray (array) {
	let sum = array.reduce((number, currentSum ) => number + currenSum)
  return sum / array.length
}
```

�� ���������� � ����������� ��� ��������� ������� ��������. ����������� ������ ����� ����������, ������� ���, ��� ����� �������� � ����� ����� � �������, ����� ������ ������.

## **8. �����������**
---
### ��� ��������� ���� ������������ �����������. ����������� �� ����������� ��������������� JavaScript.

������������ ����������� ���������� � �������� ����� `//`. �� ��� ����������� ������ ���� ������;
������������� ����������� ������������� ����� `/*` � `*/`. �� �������� ������ ����������� ����������� ������ ���� ������. ������ ����� ����������� ������������� �� ����� ������.

## **9. �������������� ���**
---
� ������� ��� ������������ ����, ������� ������� �� ����������.

� ���� ��� �����������, �� �������������� ����������

� ���� ��� ���������, �������� ������� �� ������������ � ����������, ��������� ������� ��� �������� �������� � �� ���������� ��� ��������� �������

## **10. ��������� �� ������������� ������ ����� ����**

����� ���� ������� ������������� �� Ruby, ������ ���������� ������� � ����� �����. ��� �������������� ������ ������� ��������� ������� ���� � ��������-��������������� ������. ��� ���.
+ ������ �� ������ ���� ������� 100 ����� ����.
+ ������ � ������� �� ������ ���� ������� 5 ����� ����.
+ ������� ������� ���������� �� ����� 4 ����������.
+ ����������� ����� ���������������� ���� ���� ������.
+ ���������� ���������� � [�����������](https://www.youtube.com/watch?v=npOGOmkxuio), ���������� ���� ������.

## **�����**
---
8-) � ���� ��������� �� ���������� � ���� ���������� �������������� �� ��������� ������� � ��������� ����. ������, ��� � ���� ������������. ��� � ������, �������������� ��������� ������������ ������� ��������. ���� �������������� ��������� �������, �������� ���������� �����, ��, � ��������� � �����, ��� ��������� �������� ����� �������� �� �����������, ���, ���������� � �������������� ������, ����� ���������� ����� ��������, ��� ����� ����� ���������, ������������ � ������������ ��������.