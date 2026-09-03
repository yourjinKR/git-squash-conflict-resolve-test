## 테스트 결과

AI가 제시한 방향성을 개인 저장소에 직접 테스트 진행했다.  
아래 시나리오대로 입력시 `develop`에 있는 커밋들이 전부 `develop`의 기준으로 초기화되며 tag 위치도 해시로 고정 가능하다.  
그러나, 이전에 squash 했던 커밋들과 PR은 바꿀 수 없기에 지금 수행할 이유가 크게 없다.  

```bash
git fetch --all
```

```bash
git checkout main
```

```bash
git reset --hard origin/develop
```

```bash
git tag v0.1.0 [릴리즈 시점 커밋 해시]
git tag v0.2.0 [릴리즈 시점 커밋 해시]
git push origin --tags
```

```bash
git push origin main --force
```
