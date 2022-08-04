# Overview

RecyclerView안의 뷰 클릭 시 디바이스 중간에 위치시키는 클래스입니다.<br/>
아래와 같이 dependencies에 추가하시면 사용하실 수 있습니다.

# 라이브러리 추가

maven { url "https://jitpack.io" } 를 Project Gradle에 추가.
        
```java
  dependencyResolutionManagement {
  repositoriesMode.set(RepositoriesMode.FAIL_ON_PROJECT_REPOS)
    repositories {
        google()
        mavenCentral()
        maven { url "https://jitpack.io" }
    }
  }
```

# 의존성 주입

app module gradle에 추가.

```java
  dependencies {
    implementation 'com.github.dla3946gns:RecyclerCenterView:1.0.1'
  }
```

# 사용법

특정 리사이클러뷰에 setLayoutManager() 실행 시 파라미터로 넣기.

```java
  // 레이아웃 매니저와 리사이클러뷰 초기화
  recyclerCenterView = new RecyclerCenterView(context);
  recyclerView = findViewById(R.id.rv_test);
  
  // setLayoutManager()에 파라미터로 recyclerCenterView를 넣기
  recyclerView.setLayoutManager(recyclerCenterView);
```
