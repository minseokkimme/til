## 📘 문제 설명
수많은 마라톤 선수들이 마라톤에 참여하였습니다. 단 한 명의 선수를 제외하고는 모든 선수가 마라톤을 완주하였습니다.

마라톤에 참여한 선수들의 이름이 담긴 배열 participant와 완주한 선수들의 이름이 담긴 배열 completion이 주어질 때, 완주하지 못한 선수의 이름을 return 하도록 solution 함수를 작성해주세요.

## 📕 제한사항
- 마라톤 경기에 참여한 선수의 수는 1명 이상 100,000명 이하입니다.
- completion의 길이는 participant의 길이보다 1 작습니다.
- 참가자의 이름은 1개 이상 20개 이하의 알파벳 소문자로 이루어져 있습니다.
- 참가자 중에는 동명이인이 있을 수 있습니다.

---
## 🔑 첫 풀이 방법
단순하게 for 문을 2번 써서 전체 탐색을 해서 `completion` 배열의 요소와 `participant` 배열의 요소가 같은 것은 `0`으로 대체한 다음, 마지막으로 `0`과 같지 않은 값을 `answer` 값에 넣는 방식으로 풀었다. 우선 코드를 보자면 다음과 같다.
``` java
class Solution {
    public String solution(String[] participant, String[] completion) {
        String answer = "";
        for(int i = 0; i < completion.length; i++){
            for(int j = 0; j < participant.length; j++){
                if(completion[i].equals(participant[j])){
                    participant[j] = "0";
                    break;
                }
            }
        }
        for(int i = 0; i < participant.length; i++){
            if(participant[i].equals("0") == false){
                answer = participant[i];
            }
        }
        return answer;
    }
}
```
하지만 이렇게 풀었을 때 다음과 같이 효율성 테스트에서 실패를 하게 된다.😭😭
![](https://images.velog.io/images/minseok0818/post/480b7ab2-2840-4755-9ae8-560e98596bac/image.png)

---
## 🔑 최종 풀이 방법
처음에 각 String 배열을  정렬을 하면 `participant`와 `completion` 배열이 똑같은 순서대로 들어오게 된다. 따라서 각 자리를 비교한 뒤 전부 다 같으면 마지막 요소를 `return`하는 코드를 짰다.
``` java
class Solution {
    public String solution(String[] participant, String[] completion) {
        String answer = "";
        Arrays.sort(participant);
        Arrays.sort(completion);
        int i = 0;
        for(i = 0; i<completion.length;i++){
            if(!participant[i].equals(completion[i])){
                return participant[i];
            }   
        }
        return participant[i];
    }
}
```
이렇게 하면 다음과 같이 만점을 받게 된다!!💯💯
![](https://images.velog.io/images/minseok0818/post/362a1af7-a92f-4161-b811-559250ceb9e7/image.png)
## 👨‍🎓 더 공부해야 될 점
> - 시간복잡도 생각하기!!
- 배열이 있을 때 정렬하면 이점이 있는지 찾아보기!!