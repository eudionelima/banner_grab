# banner_grab.py

Ferramenta simples em Python para captura de banners de serviços em portas específicas de um host.

## Sobre

O `banner_grab.py` conecta-se a portas TCP de um host alvo e tenta capturar o *banner* retornado pelo serviço em execução — informação útil para identificar versões de software, sistemas operacionais e serviços expostos durante reconhecimento de rede.

## Uso

```bash
python3 banner_grab.py <IP>
```

**Exemplo:**

```bash
python3 banner_grab.py 192.168.0.1
```

## Funcionalidades

-  Captura de banners em múltiplas portas
-  Timeout de 3 segundos por conexão
-  Tratamento de erros silencioso (conexões falhas não interrompem a execução)

## Requisitos

- Python 3.x
- Nenhuma dependência externa (usa apenas bibliotecas padrão)

## Aviso

Esta ferramenta deve ser utilizada **apenas em ambientes e sistemas para os quais você possui autorização explícita** para realizar testes. O uso não autorizado contra sistemas de terceiros pode violar leis locais e internacionais.

## 📄 Licença

MIT
