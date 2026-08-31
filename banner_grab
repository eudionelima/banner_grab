#!/usr/bin/env python3
# Desenvolvido por: Dione Lima
# GitHub: github.com/eudionelima

import sys
import socket

def pegar_banner(ip, portas):
    """Pega banners dos serviços nas portas especificadas."""
    banners = []
    
    for porta in portas:
        try:
            s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
            s.settimeout(3)
            s.connect((ip, porta))
            dados = s.recv(1024)
            banners.append(dados.decode('utf-8', errors='ignore'))
            s.close()
        except:
            pass
    
    return ''.join(banners)

if __name__ == "__main__":
    if len(sys.argv) < 2:
        print("Uso: python3 banner_grab.py <IP>")
        sys.exit(1)
    
    alvo = sys.argv[1]
    portas = [33024, 33054, 43001, 44289, 49222]
    
    resultado = pegar_banner(alvo, portas)
    
    if resultado.strip():
        print(f"\n[+] Banners:\n{resultado}")
    else:
        print("[-] Nenhum banner")
