# 알고리즘 문제풀이
1.직사각형 별찍기
```javascript
process.stdin.setEncoding('utf8');
process.stdin.on('data', data => {
    const n = data.split(" ");
    const a = Number(n[0]), b = Number(n[1]);
    const result = ("*").repeat(a)+("\n") // *을 a번 반복한 후 줄바꿈
    console.log((result).repeat(b)); // result를 b번 반복
});
```
2.짝수와 홀수
```javascript 
function solution(num) {
    var answer = '';
    if(num % 2 == 0){ // num을 2로 나눈 나머지값이 0이면
        answer = "Even" // 짝수
    }else( // 아니면 
        answer = "Odd" // 홀수
    )
    return answer;
}
```
3.가운데 글자 가져오기
```javascript 
function solution(s) {
    var answer = '';
    var length = s.length
    if(length % 2 != 0){ //s의 length가 홀수면
       return s.substr((length-1)/2,1) // length -1 = index / 2, 1글자
       }else { //s의 length가 짝수면
       return s.substr((length-1)/2,2) // length -1 = index / 2, 2글자
       }
}
```
4.두 정수 사이의 합
```javascript 
function solution(a, b) {
    var answer = 0;
    var max = Math.max(a,b) //a 와 b 중 최대값
    var min = Math.min(a,b) //a 와 b 중 최소값
    for(i=min;i<= max;i++){ //min가 max까지 하나씩 증가한다.
        answer += i // 대입연산자로 합계 계산
    }
    return answer;
}
```
7.음양 더하기
```javascript
function solution(absolutes, signs) {
    var answer = 0;
    var length = absolutes.length;
    for(i = 0; i < length; i++){
        if(signs[i]){ // signs가 참일 경우
            answer += absolutes[i];
        }else { // signs가 거짓일 경우
            answer += (absolutes[i]) *-1; // 음수로 곱한 것을 대입연산자로 더해준다.
        }
    }
    return answer;
}
```
15.내적
```javascript
function solution(a, b) {
    var answer = 0;
    for(i = 0;i < a.length; i++){
        answer += a[i] * b[i] //a의 i번째와 b의 i번째를 곱한 것을 대입연산자로 더해준다.
    }
    return answer;
}
```
