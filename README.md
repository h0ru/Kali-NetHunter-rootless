# Guia Instalação Kali Net-Hunter Termux (Sem Root)
![kali](https://github.com/h0ru/Kali-NetHunter-rootless/blob/main/nethunter-git-logo.png)

## Sumário
 * [Termux](#termux)
 * [Pré Instalação](#pré-instalação)
 * [NetHunter](#nethunter)
 * [Nethunter KeX](#nethunter-kex)

## Termux
### ► Download via F-Droid: 
- **[Termux](https://f-droid.org/en/packages/com.termux)**

### ► Considerações:
- O download via F-Droid nos garante uma versão mais atual comparado a da Play Store que foi **[ENCERRADA](https://github.com/termux/termux-packages/issues/6726)**
- Pode ser necessário dar permissão de instalação de fontes desconhecidas no seu aparelho!
- Site do projeto: **https://termux.dev**


## Pré Instalação
### ► Atualização:
- Hablitar outras mirrors para os repositórios (Opcional)
```
 termux-change-repo
```

- Atualizar os repositórios e o sistema
```
apt update && apt upgrade -y
```

- Habiltar a permissão de armazenamento do Termux no dispositivo
```
termux-setup-storage
```

- Instalar o Wget
```
pkg install wget
```

## NetHunter
![icon](https://gitlab.com/uploads/-/system/group/avatar/5043946/nethunter.png?width=64) 
### ► Download e Instalação do NetHunter:
- Baixar o script (O `chmod +x` já vem incluso no comando)
```
wget -O https://gitlab.com/kalilinux/nethunter/build-scripts/kali-nethunter-project/raw/master/nethunter-rootless/install-nethunter-termux ; chmod +x install-nethunter-termux
```

- Execute o script
```
./install-nethunter-termux
```

- Quando for escolher as opções de instalação, escolha a 1 (FULL)

- Após a escolha da opção apenas aguarde a instalação e configuração do NetHunter

- Quando aparecer esta mensagem `[?] Delete downloaded rootfs file? [y/N]` Apenas pressione ENTER


### ► Como usar:
```
[+] nh                    # Shortcut para o NetHunter
[+] nethunter             # Inicia o NetHunter CLI
[+] nethunter kex passwd  # Configura uma senha para o KeX
[+] nethunter kex &       # Inicia o NetHunter GUI
[+] nethunter kex stop    # Para o NetHunter GUI
[+] nethunter -r          # Rode o NetHunter como root
```

## Nethunter KeX
![icon](https://store.nethunter.com/repo/icons-640/com.offsec.nethunter.kex.11407306.png)
### ► Download e instalação dos programas necessários:
- Informações sobre o NetHunter KeX: **[INFO](https://store.nethunter.com/packages/com.offsec.nethunter.kex)**
- Download do APK do NetHunter KeX: **[APK NetHunter KeX](https://store.nethunter.com/repo/com.offsec.nethunter.kex_11407306.apk)**
- Download do APK da NetHunterStore: **[APK NetHunterStore](https://store.nethunter.com/NetHunterStore.apk)**
- Pode ser necessário dar permissões de instalação para os aplicativos! 

### ► Como usar o NetHunter KeX
- Crie uma senha para o seu KeX dentro do Termux
```
nethunter kex passwd
```

- Execute o KeX no Termux e deixe ele rodando em segundo plano
```
nethunter kex &
```

- Após a execução do comando anterior será retornado em qual porta o serviço VNC está rodando (**Por padrão será 5901**)

- Minimize o Termux e abra o NetHunter KeX... 

- No campo `VNC Server` mantenha localhost:1 e no campo `port` deixe a que estiver rodando o serviço VNC (Ex. 5901)

- No campo `VNC Password` coloque a senha que foi configurada no Termux

- Agora basta clicar em `Connect` para ter sua GUI do NetHunter


##
