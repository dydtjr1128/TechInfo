# Useful linux commands
유용한 팁


<p>
  <ul>
    <li>Valgrind -v <processName> : 메모리 관리-디버깅기능(apt-get install valgrind)</li>
  </ul>  
  <ul>
    <li>sudo ldconfig : 라이브러리 so 파일이없거나 꼬였을때 </li>
  </ul>  
</p>
   <ul>
    <li>파일 최대 개수(fd)</li>
  </ul>  
  
```
    $ sysctl fs.file-max
    fs.file-max = 775052
```
 <ul>
    <li>각 네트워크 장치 별로 커널이 처리하도록 쌓아두는 queue의 크기를 설정</li>
    <ul>
      <li>커널의 패킷 처리 속도가 이 queue에 추가되는 패킷의 인입 속도보다 떨어진다면 미처 queue에 추가되지 못한 패킷들은 버려질 것입니다.

이 커널 파라미터도 trade-off 관계가 메모리 사용량 밖에 없으므로, 적당히 증가시켜두는 것도 괜찮습니다.
다음과 같은 명령어로 설정값을 적당히 증가 시킬 수 있습니다.</li>
    </ul>
</ul> 

```
  $ sysctl -w net.core.netdev_max_backlog="30000"
```

<ul>
    <li>프로세스가 가질 수 있는 소켓 포함 파일 개수 변경</li>    
</ul> 
```
  ulimit -SHn 65535
```
