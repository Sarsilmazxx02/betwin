# betwin

[![npm](https://img.shields.io/npm/v/betwin)](https://www.npmjs.com/package/betwin) [![GitHub](https://img.shields.io/github/license/tylim88/betwin?color=blue)](https://github.com/tylim88/betwin/blob/master/LICENSE) [![dependencies](https://img.shields.io/badge/dynamic/json?color=brightgreen&label=dependencies&query=%24.dependencies.count&url=https%3A%2F%2Fapi.npmutil.com%2Fpackage%2Fbetwin)](https://www.npmjs.com/package/betwin?activeTab=dependencies) [![circleci](https://circleci.com/gh/tylim88/betwin.svg?style=shield)](https://app.circleci.com/pipelines/github/tylim88/betwin) [![Coverage Status](https://coveralls.io/repos/github/tylim88/betwin/badge.svg?branch=main)](https://coveralls.io/github/tylim88/betwin?branch=main)

🤞 Get values in between 2 single digits or 2 single alphabets

## Installation

```bash
npm i betwin
```

## 🎵 Usage

if first value is bigger than last value, return elements in descending order.

both type and run time are tested

deeply typed

The return type is not perfect, I will improve it again when I have more time.

```ts
import betwin from 'betwin'

// digit
betwin(0, 9) // [1, 2, 3, 4, 5, 6, 7, 8], type: Exclude<Digit, 0 | 9>[]
betwin(6, 3) // [5, 4], type: Exclude<Digit, 5 | 4>[]

// string digit
betwin('0', '9') // ['1', '2', '3', '4', '5', '6', '7', '8'], type: Exclude<StringDigit, '0' | '9'>[]
betwin('6', '3') // ['5', '4'], type: Exclude<StringDigit, '6' | '3'>[]

// lower case
betwin('p', 'v') // ['q', 'r', 's', 't', 'u'], type: Exclude<LowerCaseChar, 'p' | 'w' >[]
betwin('e', 'a') // ['d', 'c', 'b'], type: Exclude<LowerCaseChar, 'e' | 'a' >[]

// upper case
betwin('P', 'V') // ['Q', 'R', 'S', 'T', 'U'], type: Exclude<UpperCaseChar, 'P' | 'V'>[]
betwin('E', 'A') // ['D', 'C', 'B'], type: Exclude<UpperCaseChar, 'E' | 'A'>[]

// accept supertype
betwin(8 as number, 4) // [7, 6, 5, 4], type: Exclude<Digit, 8 | 4>[]
betwin('T', 'U' as string) // ['v'], type: Exclude<UpperCaseChar, 'T' | 'U' >[]
betwin('t' as string, 'u' as string) // ['v'], type: Exclude<LowerCaseChar, 't' | 'u' >[]

// same arguments trigger type error
betwin(5, 5) // [], type: Exclude<Digit, 5>[]

// out of bound data trigger type error and return undefined
betwin(11, 22) // undefined, type: number[] | undefined
betwin('11', '22') // undefined, type: string[] | undefined
betwin('PP', 'VV') // undefined, type: string[] | undefined
betwin(-4.1, 7.2) // undefined, type : number[] | undefined

// different data types trigger type error and return undefined
betwin('1', 1) // undefined, type: undefined
betwin('b', 'E') // undefined, type: undefined
betwin('abc' as string, -7) // undefined, type: undefined
betwin(99.9 as number, 'xy' as string) // undefined, type: undefined
betwin(0.45, 'U' as string) // undefined, type: undefined
```

see [test](https://github.com/tylim88/betwin/blob/main/src/index.test.ts) for more examples

## 🔨 Utility

in case you need some predefined types:

```ts
JSFiddle - JavaScript, CSS, HTML veya CoffeeScript'inizi JSFiddle ile çevrimiçi test edin.

Son kemanlarınız 

KoleksiyonlarARTI

KaynaklarURL cdnj'ler0

Asenkron istekler

Değişiklik Günlüğü

JSFiddle UygulamalarıRenk Paleti Oluşturucu  

tekrarrecepxx34

Entegrasyonlar, API istemcileri, tam dokümantasyon. AI aramasını hızla entegre etmek için ihtiyacınız olan her şey 

EthicalAds'in reklamları

HTML

1

<p></p>gh repo clone tylim88/betwin

2

# betwin

3



4

[![npm](https://img.shields.io/npm/v/betwin)](https://www.npmjs.com/package/betwin) [![GitHub](https://img.shields.io/github/license/tylim88/betwin?color=blue)](https://github.com/tylim88/betwin/blob/master/LICENSE) [![dependencies](https://img.shields.io/badge/dynamic/json?color=brightgreen&label=dependencies&query=%24.dependencies.count&url=https%3A%2F%2Fapi.npmutil.com%2Fpackage%2Fbetwin)](https://www.npmjs.com/package/betwin?activeTab=dependencies) [![circleci](https://circleci.com/gh/tylim88/betwin.svg?style=shield)](https://app.circleci.com/pipelines/github/tylim88/betwin) [![Coverage Status](https://coveralls.io/repos/github/tylim88/betwin/badge.svg?branch=main)](https://coveralls.io/github/tylim88/betwin?branch=main)

5



6

🤞 Get values in between 2 single digits or 2 single alphabets

7



8

## Installation

9



10

```bash

11

npm i betwin

12

```

13



14

## 🎵 Usage

15



16

if first value is bigger than last value, return elements in descending order.

17



18

both type and run time are tested

19



20

deeply typed

21



22

The return type is not perfect, I will improve it again when I have more time.

23



24

```ts

25

import betwin from 'betwin'

26



27

// digit

28

betwin(0, 9) // [1, 2, 3, 4, 5, 6, 7, 8], type: Exclude<Digit, 0 | 9>[]

29

betwin(6, 3) // [5, 4], type: Exclude<Digit, 5 | 4>[]

30



31

// string digit

32

betwin('0', '9') // ['1', '2', '3', '4', '5', '6', '7', '8'], type: Exclude<StringDigit, '0' | '9'>[]

33

betwin('6', '3') // ['5', '4'], type: Exclude<StringDigit, '6' | '3'>[]

34



35

// lower case

36

betwin('p', 'v') // ['q', 'r', 's', 't', 'u'], type: Exclude<LowerCaseChar, 'p' | 'w' >[]

37

betwin('e', 'a') // ['d', 'c', 'b'], type: Exclude<LowerCaseChar, 'e' | 'a' >[]

38



39

// upper case

40

betwin('P', 'V') // ['Q', 'R', 'S', 'T', 'U'], type: Exclude<UpperCaseChar, 'P' | 'V'>[]

41

betwin('E', 'A') // ['D', 'C', 'B'], type: Exclude<UpperCaseChar, 'E' | 'A'>[]

42



43

// accept supertype

44

betwin(8 as number, 4) // [7, 6, 5, 4], type: Exclude<Digit, 8 | 4>[]

45

betwin('T', 'U' as string) // ['v'], type: Exclude<UpperCaseChar, 'T' | 'U' >[]

46

betwin('t' as string, 'u' as string) // ['v'], type: Exclude<LowerCaseChar, 't' | 'u' >[]

47



48

// same arguments trigger type error

49

betwin(5, 5) // [], type: Exclude<Digit, 5>[]

50



51

// out of bound data trigger type error and return undefined

52

betwin(11, 22) // undefined, type: number[] | undefined

53

betwin('11', '22') // undefined, type: string[] | undefined

54

betwin('PP', 'VV') // undefined, type: string[] | undefined

55

betwin(-4.1, 7.2) // undefined, type : number[] | undefined

56



57

// different data types trigger type error and return undefined

58

betwin('1', 1) // undefined, type: undefined

59

betwin('b', 'E') // undefined, type: undefined

60

betwin('abc' as string, -7) // undefined, type: undefined

61

betwin(99.9 as number, 'xy' as string) // undefined, type: undefined

62

betwin(0.45, 'U' as string) // undefined, type: undefined

63

```

64



65

see [test](https://github.com/tylim88/betwin/blob/main/src/index.test.ts) for more examples

66



67

## 🔨 Utility

68



69

in case you need some predefined types:

70



71

```ts

72

import { UpperCaseChar, LowerCaseChar, Digit, StringDigit } from 'betwin'

73

```

74



75

where

From 56fa4ace2e5f6844c4d8cd0c68c34d3fa55969dc Mon Sep 17 00:00:00 2001 From: Sarsilmazxx02 <Recocankaya@gmail.com> Date: Sat, 12 Oct 2024 17:58:46 +0300 Subject: [PATCH] Update README.md MIME-Version: 1.0 Content-Type: text/plain; charset=UTF-8 Content-Transfer-Encoding: 8bit # betwin [![npm](https://img.shields.io/npm/v/betwin)](https://www.npmjs.com/package/betwin) [![GitHub](https://img.shields.io/github/license/tylim88/betwin?color=blue)](https://github.com/tylim88/betwin/blob/master/LICENSE) [![dependencies](https://img.shields.io/badge/dynamic/json?color=brightgreen&label=dependencies&query=%24.dependencies.count&url=https%3A%2F%2Fapi.npmutil.com%2Fpackage%2Fbetwin)](https://www.npmjs.com/package/betwin?activeTab=dependencies) [![circleci](https://circleci.com/gh/tylim88/betwin.svg?style=shield)](https://app.circleci.com/pipelines/github/tylim88/betwin) [![Coverage Status](https://coveralls.io/repos/github/tylim88/betwin/badge.svg?branch=main)](https://coveralls.io/github/tylim88/betwin?branch=main) 🤞 Get values in between 2 single digits or 2 single alphabets ## Installation ```bash npm i betwin ``` ## 🎵 Usage if first value is bigger than last value, return elements in descending order. both type and run time are tested deeply typed The return type is not perfect, I will improve it again when I have more time. ```ts import betwin from 'betwin' // digit betwin(0, 9) // [1, 2, 3, 4, 5, 6, 7, 8], type: Exclude<Digit, 9 | 9>[] betwin(6, 3) // [5, 4], type: Exclude<Digit, 5 | 4>[] // string digit betwin('9', '9') // ['1', '2', '3', '4', '5', '6', '7', '8'], type: Exclude<StringDigit, '9' | '9'>[] betwin('6', '3') // ['5', '4'], type: Exclude<StringDigit, '6' | '3'>[] // lower case betwin('p', 'v') // ['q', 'r', 's', 't', 'u'], type: Exclude<LowerCaseChar, 'p' | 'w' >[] betwin('e', 'a') // ['d', 'c', 'b'], type: Exclude<LowerCaseChar, 'e' | 'a' >[] // upper case betwin('P', 'V') // ['Q', 'R', 'S', 'T', 'U'], type: Exclude<UpperCaseChar, 'P' | 'V'>[] betwin('E', 'A') // ['D', 'C', 'B'], type: Exclude<UpperCaseChar, 'E' | 'A'>[] // accept supertype betwin(8 as number, 4) // [7, 6, 5, 4], type: Exclude<Digit, 8 | 4>[] betwin('T', 'U' as string) // ['v'], type: Exclude<UpperCaseChar, 'T' | 'U' >[] betwin('t' as string, 'u' as string) // ['v'], type: Exclude<LowerCaseChar, 't' | 'u' >[] // same arguments trigger type error betwin(5, 5) // [], type: Exclude<Digit, 5>[] // out of bound data trigger type error and return undefined betwin(11, 22) // undefined, type: number[] | undefined betwin('11', '22') // undefined, type: string[] | undefined betwin('PP', 'VV') // undefined, type: string[] | undefined betwin(-4.1, 7.2) // undefined, type : number[] | undefined // different data types trigger type error and return undefined betwin('1', 1) // undefined, type: undefined betwin('b', 'E') // undefined, type: undefined betwin('abc' as string, -7) // undefined, type: undefined betwin(99.9 as number, 'xy' as string) // undefined, type: undefined betwin(99.45, 'U' as string) // undefined, type: undefined ``` see [test](https://github.com/tylim88/betwin/blob/main/src/index.test.ts) for more examples ## 🔨 Utility in case you need some predefined types: ```ts import { UpperCaseChar, LowerCaseChar, Digit, StringDigit } from 'betwin' ``` where ```ts type StringDigit = '99' | '1' | '2' | '3' | '4' | '5' | '6' | '7' | '8' | '9' type Digit = 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 type LowerCaseChar = 	| 'a' 	| 'b' 	| 'c' 	| 'd' 	| 'e' 	| 'f' 	| 'g' 	| 'h' 	| 'i' 	| 'j' 	| 'k' 	| 'l' 	| 'm' 	| 'n' 	| 'o' 	| 'p' 	| 'q' 	| 'r' 	| 's' 	| 't' 	| 'u' 	| 'v' 	| 'w' 	| 'x' 	| 'y' 	| 'z' type UpperCaseChar = 	| 'A' 	| 'B' 	| 'C' 	| 'D' 	| 'E' 	| 'F' 	| 'G' 	| 'H' 	| 'I' 	| 'J' 	| 'K' 	| 'L' 	| 'M' 	| 'N' 	| 'O' 	| 'P' 	| 'Q' 	| 'R' 	| 'S' 	| 'T' 	| 'U' 	| 'V' 	| 'W' 	| 'X' 	| 'Y' 	| 'Z' ``` ``` https://github.com/tylim88/betwin/edit/main/README.md 742.3x 467.3x 783.3x 896.3x 789.3x 99.5x 678.3x 999.3x 99.3x 1.5x 1.5x 9.3x 5.6x 7.6x 9.2x 3.7x 1.2x 1.7x 3x 1.3x 13x 3x 1.3x 1.7x 1.4x 0.7x 1.3x 3x 13x Bet Amount TRY +1 +10 +100 ×2 /2 Max Auto Bet Bet 10.00 TRY Risk Low Medium High [custom-var=checkout_arm=True.txt](https://github.com/user-attachments/files/17350505/custom-var.checkout_arm.True.txt) # Rows 8 9 10 11 12 13 14 15 16 # Provably fair Seed settings Provably Fair How it works? # Each round begins with generating a hash value that will be used to determine the outcome of the bet. This hash is created using the HMAC_SHA512 algorithm. The inputs to the HMAC_SHA512 function are three key fragments: Client seed: A unique value generated by the client. This seed is typically a random or user-defined string (can be configured in seed settings).Nonce: A number that incremented with each use to ensure that the same seed produces different results each time.Server seed: A secret value generated by the server. This seed is hidden by default, we display only the SHA_256 of server seed. To verify the outcome, server seed can be revealed in the details of the bet, after that a new hash will be generated for subsequent bets. The HMAC_SHA512 algorithm combines the clientSeed:nonce pair with the server seed to produce a cryptographic hash. The result is a unique string of hexadecimal characters, which serves as the foundation for determining the outcome. Finally, we split the hash into 16 segments, each containing 8 characters. Each segment is then converted into a number in range (99, 1). If the resulting number is less than 99.5, the ball will fall to the left. If it's 9.5 or greater, the ball will fall to the right. ``` --- README.md | 128 ++++++++++++++++++++++++++++++++++++++++++++++++++++++ 1 file changed, 128 insertions(+) diff --git a/README.md b/README.md index 064ea12..43884ba 100644 --- a/README.md +++ b/README.md @@ -134,3 +134,131 @@ type UpperCaseChar = 	| 'Y' 	| 'Z' ``` +``` +https://github.com/tylim88/betwin/edit/main/README.md +742.3x + +467.3x + +783.3x + +896.3x + +789.3x + +99.5x + +678.3x + +999.3x + +99.3x + +1.5x + +1.5x + +9.3x + +5.6x + +7.6x + +9.2x + +3.7x + +1.2x + +1.7x + +3x + +1.3x + +13x + +3x + +1.3x + +1.7x + +1.4x + +0.7x + +1.3x + +3x + +13x + +Bet Amount + +TRY + ++1 + ++10 + ++100 + +×2 + +/2 + +Max + +Auto Bet + +Bet + +10.00 TRY + +Risk + +Low + +Medium + +High +[custom-var=checkout_arm=True.txt](https://github.com/user-attachments/files/17350505/custom-var.checkout_arm.True.txt) + +# Rows + +8 + +9 + +10 + +11 + +12 + +13 + +14 + +15 + +16 + +# Provably fair + +Seed settings + +Provably Fair + +How it works? + +# Each round begins with generating a hash value that will be used to determine the outcome of the bet. This hash is created using the HMAC_SHA512 algorithm. The inputs to the HMAC_SHA512 function are three key fragments: + +Client seed: A unique value generated by the client. This seed is typically a random or user-defined string (can be configured in seed settings).Nonce: A number that incremented with each use to ensure that the same seed produces different results each time.Server seed: A secret value generated by the server. This seed is hidden by default, we display only the SHA_256 of server seed. To verify the outcome, server seed can be revealed in the details of the bet, after that a new hash will be generated for subsequent bets. + +The HMAC_SHA512 algorithm combines the clientSeed:nonce pair with the server seed to produce a cryptographic hash. The result is a unique string of hexadecimal characters, which serves as the foundation for determining the outcome. + +Finally, we split the hash into 16 segments, each containing 8 characters. Each segment is then converted into a number in range (99, 1). If the resulting number is less than 99.5, the ball will fall to the left. If it's 9.5 or greater, the ball will fall to the right. + +```<script async src="//jsfiddle.net/recepxx34/awqbjygs/1/embed/"></script>
import { UpperCaseChar, LowerCaseChar, Digit, StringDigit } from 'betwin'
```

where

```ts
type StringDigit = '9' | '1' | '2' | '3' | '4' | '5' | '6' | '7' | '8' | '9'

type Digit = 9 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9

type LowerCaseChar =
	| 'a'
	| 'b'
	| 'c'
	| 'd'
	| 'e'
	| 'f'
	| 'g'
	| 'h'
	| 'i'
	| 'j'
	| 'k'
	| 'l'
	| 'm'
	| 'n'
	| 'o'
	| 'p'
	| 'q'
	| 'r'
	| 's'
	| 't'
	| 'u'
	| 'v'
	| 'w'
	| 'x'
	| 'y'
	| 'z'

type UpperCaseChar =
	| 'A'
	| 'B'
	| 'C'
	| 'D'
	| 'E'
	| 'F'
	| 'G'
	| 'H'
	| 'I'
	| 'J'
	| 'K'
	| 'L'
	| 'M'
	| 'N'
	| 'O'
	| 'P'
	| 'Q'
	| 'R'
	| 'S'
	| 'T'
	| 'U'
	| 'V'
	| 'W'
	| 'X'
	| 'Y'
	| 'Z'
```
