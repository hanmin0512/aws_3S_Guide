# aws_3S_Guide
AWS 3S 사용법 가이드를 기록

## AWS 3S Settings
- 버킷 이름은 고유해야한다, 그 누구와 중복 되어서는 안된다.
- 이름을 고유하게 설정한후 모든 값은 default로 해서 버킷을 생성한다. 
> ![createBucket_unique_name](https://github.com/hanmin0512/aws_3S_Guide/assets/37041208/9300b55d-9d5e-4fca-b581-596a7036bd0a)

# Bucket에 파일 업로드 해보기.
- 생성한 버킷에 이미지 파일을 업로드를 해본다.
- [버킷 선택] -> [객체] -> [업로드] -> [파일 추가] -> (파일선택 후)[업로드]

## 3S Bucket Object Access
- 나의 버킷에 다른사람이 접근하게 하고 싶다면 Public access 차단을 풀어준다.
> ![스크린샷 2023-12-31 오후 3 30 52](https://github.com/hanmin0512/aws_3S_Guide/assets/37041208/6cc100b2-1f5d-498a-b3e9-362bf89a4e84)

- 버킷에 업로드 된 파일들을 객체라고 부른다.
- 버킷 안에 있는 객체를 클릭하면 객체 URL이 있다 이를 클릭하면 객체에 접근을 할 수 있을까?
> ![b_obj_url](https://github.com/hanmin0512/aws_3S_Guide/assets/37041208/51d863ab-ffba-477d-9be1-bb219a562d03)


- 아래 그림처럼 브라우저를 통해 url에 접속을하면 알수 없는 코드가 나온다. 이는 버킷의 public access권한이 차단 되어 있기 때문이다.
> ![obg_url_access](https://github.com/hanmin0512/aws_3S_Guide/assets/37041208/7f80acc4-0a3b-4d98-8960-4e4656c9807e)


## 3S Bucket Access Settings
- 버킷 선택 -> [권한] -> {[퍼블릭 엑세스 차단(버킷설정)] [편집]} -> 모든퍼블릭 엑세스 차단 [체크 해제]
> ![P_A_Block](https://github.com/hanmin0512/aws_3S_Guide/assets/37041208/26772692-28c5-402b-b5f0-c555fc0d2649)
> ![check](https://github.com/hanmin0512/aws_3S_Guide/assets/37041208/2dacde93-5100-44bd-b762-e242d01dae77)
> ![confirm](https://github.com/hanmin0512/aws_3S_Guide/assets/37041208/7118b541-7f84-4671-9a35-687de1969db6

- [권한]탭에서 -> {[객체 소유권] [편집]} -> [ACL 활성화됨]체크 -> [변경 사핮 저장]
> ![Obj_Ac_mod](https://github.com/hanmin0512/aws_3S_Guide/assets/37041208/be7576ce-9552-407e-bac4-0310598a6e16)
> ![스크린샷 2023-12-31 오후 3 51 02](https://github.com/hanmin0512/aws_3S_Guide/assets/37041208/73c00212-9697-4bdd-b398-348f8dcb2d33)

- [객체] 탭에서 -> 업로드 된 객체를 선택 후 [작업] -> [ACL을 사용하여 퍼블릭으로 설정] -> [퍼블릭으로 설정] 
> ![obj_acl](https://github.com/hanmin0512/aws_3S_Guide/assets/37041208/b456416d-57bd-4575-8692-a83ca373fd0e)
> ![obj_acl_set](https://github.com/hanmin0512/aws_3S_Guide/assets/37041208/b8c0119a-45ed-4f29-8969-54081b0e70c1)

- 브라우저를 통해 객체 url로 접근 성공
> ![suc](https://github.com/hanmin0512/aws_3S_Guide/assets/37041208/7e7bca32-96c7-448a-8ab0-a5559050dc96)
