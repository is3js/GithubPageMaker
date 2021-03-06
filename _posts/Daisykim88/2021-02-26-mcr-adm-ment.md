---
layout: post
current: post 
cover:  assets/built/images/test.jpg
navigation: True
title: 입원환자-대면멘트  
date: 2021-02-26 08:00:00
tags: [MCR, 입원환자관리, 멘트] 
class: post-template 
subclass: 'post tag-python' 
author: daisykim88  
toc: true
---

### 초진차트 뽑기 -> 가서 뵙기

- 주소/주민번호로 동명이인 감볍



### 1. C/C 

#### 주치의 소개 

    ```
    주치의 맡게될 조재성이라고 합니다. 어디가 아프신지 여쭤보고, 안내사항 몇가지 전달하러 왔습니다.
    어디가 제일 아프세요
    ```

#### 자보용 통증악화기 

- **부위 물어보기**
- **특정상황에서** 아픈지 물어보기(계단, 평지, 앉아있을 때)
  - 자세 부담되는거 알려주면서 쉬라고 하기
- **통증악화기** 설명
  ```통증악화기라고 해서 일주일 동안은 <내가 실제로 다친 것>과 <사고로 긴장해서 느끼는 것>이 다른 경우가 많다. 
  치료와 상관없이 일주일간은 맞춰지는 단계라고 보면 된다.
  일주일동안 통증이 올라갈 수 있다. 원래 다친 부분이라서 천천히 쉬면서 치료해보겠습니다.
  ```
- **한약** 설명
  ```
  약 드시는 것도, 사람마다 체질이 달라서  드시고 배가 부글부글
  ```
  - 오늘은 **간수치가 높게 나와서, lab검사 결과 나오면 보고 말씀드릴게요**



#### 의보용 ROM, Motor, P/E 검사 루틴

- 목
  - 뒤에 서서
    - `Flexion(45)`
    - `Extension(45)` : 뒤로 한번 넘어가셨다가, 앞으로 구부려 볼게요. 아프시면 안해도 되도.
    - `Lateral bending(45/45)` : 옆으로 넘어가보실까요?
    - `Rotation(60/60)` : 옆으로 한번 비틀어 보실까요?

- 허리

  - 제 어깨에 손을 올리고 

    - `Flexion(80)`
    - `Extension(20)` : 뒤로 한번 넘어가셨다가, 앞으로 구부려 볼게요. 아프시면 안해도 되도.
    - `Lateral bending(30/30)` : 옆으로 넘어가보실까요?
    - `Rotation(60/60)` : 옆으로 한번 비틀어 보실까요?

    ```
    <C-Spine check>
    ROM
     Flexion         45
     Extension       45
     Lat. bending   45/45
     Rotation       60/60
    
    <L-Spine check>
    ROM
     Flexion         80
     Extension       20
     Lat. bending   30/30
     Rotation       60/60
    ```

    

- Motor MMT

  - **동작을 해보세요~ 시켜봐서 한다** : `3이상`

    - **못한다** : 1 or 2
      - 중력없으면 한다 : `2`
      - 약간 까닥한다 : `1`
      - 아예 힘도 안들어간다 : `0`

  - **잡아서 저항을 주는데 한다 "비슷하세요~?"** :  4이상

    - 둘다 강력하게 힘이 들어온다 : `5`
    - 한쪽이 약하다 : `약한쪽 4`

    ```
    <C-Spine check>
    Motor
     Elbow flexion(C6)      5/5
     Elbow extension(C7)      5/5
     Thumb extension(C8)      5/5
    
    <L-Spine check>    
    Motor
     Dorsiflexion(L4)       5/5
     Big toe extension(L5)  5/5
     Plantarflexion(S1)      5/5
    ```

    

- sensory

  - ++++/++++ : 둘다 똑같

  - ++++/+++ :  왼쪽 **조금 감각(25%)** 떨어짐

  - ++++/++ : 왼쪽 **1/3 이상(50%이상)** 떨어짐

  - ++++/+ : 왼쪽 **아예 감각 없음(75%이상)** 떨어짐

    ```
    <C-Spine check>
    Sensory
     C6     ++++/++++
     C7     ++++/++++
     C8     ++++/++++
        
    <L-Spine check>
    Sensory
     L4              ++++/++++
     L5              ++++/++++
     S1              ++++/++++
    ```

    

  

  

- 이학적검사

  - SLRT -> bragard -> patrick test

    ```
    <L-Spine check>
    Special test
     SLR          80/80
     Bragard      -/-
     Patrick      -/-
    ```



- 그외, 어깨, 팔꿈치, 무릎, 손목, 발목

  ```
  <Shoulder check>
  ROM
   Flexion         180/180
   Extension       45/45
   Adduction       45/45
   Abduction       180/180
   Int. rotation   60/60
   Ext. rotation   60/60
  Special test
   Apley's scratch test -/-
   Drop arm test        -/-
   Empty can test       -/-
  
  
  <Elbow check>
  ROM
   Flexion      135/135            
   Extension    0/0
   Pronation    -/-
   Supination   -/-
  
  
  <Knee check>
  ROM
   Flexion 130/130
   Extension   0/0
  Special test
   Anterior draw sign         -/-
   Posterior draw sign        -/-
   Medial collateral ligament test   -/-
   Lateral collateral ligament test   -/-
   Apley compression test -/-
  
  
  <Wrist Check>
  Flexion   75/75
  Extension 70/70
  Radial    20/20
  Ulnar     35/35
  
  
  <Ankle Check>
  ROM
   Dorsiflexion    20/20
   Plantar flexion 50/50
   Inversion       35/35
   Eversion        25/25
  ```

  





### 2. 수면(진통제)

#### 전일 사고 입원

- 전일 아파서 못잤다면 진통제 콜이 온다. 첫날에는 잘 안준다. 이 때, PAD 1일차 진통제는 잘 안나오므로 deal을 한다.

- **대전제 : `어제 잘 주무셨나요? 혹시 진통제가 필요하세요?`**

  - 필요하다. -> **`의뢰`**
    - reject 당할시 설득

- **`잘 모르겠다.`**

  1. `진통제를 먹으면, 통증이 사라져서 통증 부위를 제대로 파악 못하므로, 수면저하가 아니라면, 치료를 위해서는 몇일 참아보는게 좋다.` `너무 아프시면 진통제를 드시는게 낫다`

  두통 등에 대해서는 `한방약이 있기 때문에 오늘은 한방약을 드셔보고 참아보시고 효과가 안좋으면 진통제를 드리겠다.`

  2. 다른약물을 많이 드시는 경우
     `혈액검사 결과가 안나와서, 간기능 등을 확인한 뒤 진통제 처리하는 것이 안전하다.`

     

     

- 당일 오전사고 입원
  - 잘 주무셨는지 못 물어보니, 대전제 : **`진통제가 필요하세요?`**라고 물어본다.





#### 불면호소

야간에 수면제를 드릴 수 없으니 (평소에도 수면제x 수면유도제)

1. **`기존에 불면으로 드시는 약이 있으신가요?`**
2. **`집에 소지한 자가약이 있는가?`**
3. **`한방약 한번 드셔보세요`**



### 3. 지참약 확인 (for 추후 consult)

병동에서 해주지만, 나름대로 따로 해야한다.

1. OS 가서 W-med(양약)을 받았으면, **`약 지참하셨나요?`**

2. **P/H 상 고혈압 -> `혈압약은 안드시나요?`**
   - **`언제부터 드셨나요?`**
   - **`어디서 진단받아서 받았나요?`**
     - local FM or IM, 대학병원
   - **`최근에 언제, 몇일분 받으셨는지`**
   - **`지참약이 충분하신 가요?`**
     - 외출이 안되니, 의뢰를 드려야함.
     - 이미 로컬에서 처방받았는데 안가져왔다면, **응급으로 3~7일치**만 처방해준다. 
     - 지인이나 가족 통해서 가져오라고 해야한다. 

3. 아스피린 왜 드시나요?? 등 **진통제 의뢰시 필요한 복용약들을 조회**


### 4. 안내

1. **침치료후 뻐근**할 수 있다는 것을 고지, **약 먹고 배가 부글부글** 할 수 도 있다고 고지
   - 치료할 때, **`침 많이 맞아보셨어요? 한약 먹으면 체질에 따라 배가 부글부글 끓을 수도 있어요. `**
2. 병실생활주의사항(시끄럽게, 통화), 특이사항 발생시 안내(콜밸)
3. **`침상안정 안내(아프시면 움직이지 말고, 누워계세요.)`**
   - 진통제 원하면 바로 줘야한다.
4. 코로나로 **외출, 면회 안된다.**
   - 빨래 등 때문에, **`1층에서 마스크 끼고 간단하게 만남. 편의점까지는 가능 그 이후 가면 안됨`**
   - **`무단 외박시 퇴원`**

5. 주치의보고 바로 **EKG찍으러 가기**