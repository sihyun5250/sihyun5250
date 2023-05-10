``` java
import java.util.Arrays;

class Solution {
    public String solution(String s) {
        //1. return 값
        String answer = "";
        
        //2. String을 char[] 형태로 변환
        char[] charArr = s.toCharArray();
        //3. 변수 answer에 char[0] 배열의 첫번째 값을 담음
        answer = answer + charArr[0];
        
        //4 배열 크기만큼 for문을 돌면서 다음 글자와 비교
        for(int i=1; i<charArr.length; i++){
            
            if(Character.compare(charArr[i-1], charArr[i]) > 0){
                answer = answer + charArr[i];
            }else{
		    answer = charArr[i] + answer;	
		} 
        
	 } 
        return answer;
    }
}

```
