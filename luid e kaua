import os

ARQUIVO = "alunos.txt"

def limpar():
    os.system('cls' if os.name == 'nt' else 'clear')

def pause():
    input("\nPressione ENTER...")

def add():
    with open(ARQUIVO, "a", encoding="utf-8") as f:
        f.write(f"{input('ID: ')}|{input('Nome: ')}|{input('Matrícula: ')}|{input('Turma: ')}\n")
    print("OK")

def listar():
    if not os.path.exists(ARQUIVO):
        print("Sem dados")
        return
    with open(ARQUIVO, "r", encoding="utf-8") as f:
        for l in f:
            try:
                i, n, m, t = l.strip().split("|")
                print(i, n, m, t)
            except:
                pass

def buscar():
    if not os.path.exists(ARQUIVO):
        print("Sem dados")
        return
    x = input("ID: ")
    with open(ARQUIVO, "r", encoding="utf-8") as f:
        for l in f:
            try:
                i, n, m, t = l.strip().split("|")
                if i == x:
                    print(n, m, t)
                    return
            except:
                pass
    print("Não encontrado")

while True:
    limpar()
    print("[1] Add\n[2] Listar\n[3] Buscar\n[0] Sair")
    op = input("Escolha: ")

    if op == "0":
        break
    elif op == "1":
        add()
    elif op == "2":
        listar()
    elif op == "3":
        buscar()
    else:
        print("Inválido")

    pause()
