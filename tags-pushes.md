1) Preparar o codigo
```bash
git switch main
git pull origin main # Sincronizar com o remoto
```

2) Validar o estado
```bash
git log --oneline 5 # Ver os ultimos commits
git status # Confirmar as alteraçoes que serao comitadas ou ja estao stageadas
```

3) Criar a tag anotada
```bash
git tag -a vMAJOR.MINOR.PATCH -m "feat/fix/conventional: Mensagem de versao"
```

4) Push
```bash
git push origin main
```

5) Tag
```bash
git push origin TAG
```

---
```bash
# 1. Trabalhe na branch de correção
git switch -c fix/ldap-auth-bug

# 2. Faça o commit semântico
git commit -m "fix(ldap): corrigir timeout na autenticação"

# 3. Volte para main e faça merge
git switch main
git merge fix/ldap-auth-bug

# 4. AGORA siga a ordem correta:
git pull origin main          # Sincronize
git tag -a v1.0.1 -m "fix: timeout LDAP"  # Crie tag
git push origin main          # Envie código
git push origin v1.0.1        # Envie tag
```
