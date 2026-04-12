# Atividade 3 - Learn Git Branching

Comandos salvos durante os exercícios do site [learngitbranching.js.org](https://learngitbranching.js.org/?locale=pt_BR). Criei um arquivo .txt e um README para melhor visualização.

---

## ABA MAIN

### Seção 1 - Sequência Introdutória

**Item 1 - Introdução aos commits no Git**
```
git commit
git commit
```

**Item 2 - Branches no Git**
```
git checkout -b bugFix
```

**Item 3 - Merge no Git**
```
git checkout -b bugFix
git commit
git checkout main
git commit
git merge bugFix
```

**Item 4 - Introdução ao rebase**
```
git checkout -b bugFix
git commit
git checkout main
git commit
git checkout bugFix
git rebase main
```

---

### Seção 2 - Acelerando

**Item 1 - Solte a sua cabeça**
```
git checkout C4
```

**Item 2 - Referências relativas (^)**
```
git checkout bugFix^
```

**Item 3 - Referências relativas #2 (~)**
```
git branch -f main C6
git branch -f bugFix C0
git checkout C1
```

**Item 4 - Revertendo mudanças no Git**
```
git reset HEAD~1
git checkout pushed
git revert HEAD
```

---

### Seção 3 - Movendo trabalho por aí

**Item 1 - Introdução ao cherry-pick**
```
git cherry-pick C3 C4 C7
```

**Item 2 - Introdução ao rebase interativo**
```
git rebase -i HEAD~4
```

---

### Seção 4 - Sortidos

**Item 1 - Pegando um único commit**
```
git rebase -i HEAD~3
git cherry-pick C4
```

**Item 2 - Malabarismo com commits**
```
git rebase -i HEAD~2
git commit --amend
git rebase -i HEAD~2
git branch -f main HEAD
```

**Item 3 - Malabarismo com commits #2**
```
git checkout main
git cherry-pick C2
git commit --amend
git cherry-pick C3
```

**Item 4 - Tags no Git**
```
git tag v0 C1
git tag v1 C2
git checkout v1
```

**Item 5 - Git Describe**
```
git describe main
git describe side
git commit
```

---

### Seção 5 - Temas Avançados

**Item 1 - Fazendo mais de 9000 rebases**
```
git rebase main bugFix
git rebase bugFix side
git rebase side another
git rebase another main
```

**Item 2 - Múltiplos pais**
```
git branch bugWork main~^2~
```

**Item 3 - Espaguete de branches**
```
git checkout one
git cherry-pick C4 C3 C2
git checkout two
git cherry-pick C5 C4 C3 C2
git branch -f three C2
```

---

## ABA REMOTE

### Seção 1 - Push & Pull — repositórios remotos no Git!

**Item 1 - Introdução à clonagem**
```
git clone
```

**Item 2 - Branches remotas**
```
git commit
git checkout o/main
git commit
```

**Item 3 - Git Fetch**
```
git fetch
```

**Item 4 - Git Pull**
```
git pull
```

**Item 5 - Simulando trabalho em equipe**
```
git clone
git fakeTeamwork main 2
git fetch
git merge o/main
```

**Item 6 - Git Push**
```
git commit
git commit
git push
```

**Item 7 - Histórico divergente**
```
git clone
git fakeTeamwork
git fetch
git rebase o/main
git push
```

**Item 8 - Main bloqueado**
```
git reset --hard o/main
git checkout -b feature C2
git push origin feature
```

---

### Seção 2 - Até a origin e além — repositórios remotos avançados!

**Item 1 - Push Main!**
```
git fetch
git rebase o/main side1
git rebase side1 side2
git rebase side2 side3
git rebase side3 main
git push
```

**Item 2 - Merge com remotos**
```
git checkout main
git pull
git merge side1
git merge side2
git merge side3
git push
```

**Item 3 - Seguindo remotos**
```
git checkout -b side o/main
git commit
git pull --rebase
git push
```

**Item 4 - Parâmetros do git push**
```
git push origin main
git push origin foo
```

**Item 5 - Parâmetros do git push -- expandido**
```
git push origin main~1:foo
git push origin foo:main
```

**Item 6 - Parâmetros do fetch**
```
git fetch origin foo:main
git fetch origin main~1:foo
git checkout foo
git merge main
```

**Item 7 - Origem vazia**
```
git push origin :foo
git fetch origin :bar
```

**Item 8 - Parâmetros do pull**
```
git pull origin bar:foo
git pull origin main:side
```
