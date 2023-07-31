```java
import java.util.*;

class Solution {
    public int[] solution(String[] name, int[] yearning, String[][] photo) {
        int[] answer = new int[photo.length];
       
        HashMap<String,Integer> memory = new HashMap();
        
        //1. name[i]와 yearning[i]는 <이름-점수> 관계
        //2. map에 <키-value> 형태로 담는다.
        for(int i=0; i<yearning.length; i++){
            memory.put(name[i], yearning[i]);
        }
        
        //3. photo는 다차원배열
        for(int i=0; i<photo.length; i++){
            int sum = 0;
            //4. photo[i]번째를 돌면서
            for(int j=0; j<photo[i].length; j++){
                //5. memory<키-value>에 담긴 값이 있다면
                if(memory.containsKey(photo[i][j])){
                    //6. 점수를 합산한다.
                    sum += memory.get(photo[i][j]);   
                }
            }
            //7. answer[i]에 담는다.
            answer[i] = sum;
        }
        
        return answer;
    }
}
```
![image](https://github.com/sihyun5250/sihyun5250/assets/52738150/37a55cd9-0628-4e25-8ba6-3d394fd7fdab)
