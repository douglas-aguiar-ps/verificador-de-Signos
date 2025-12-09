# verificador-de-Signos
Verificador de signos - Atividade Faculdade Pitágoras 

from datetime import datetime

def descobrir_signo(dia: int, mes: int) -> str:
    """Retorna o signo baseado no dia e mês de nascimento."""
    
    if (dia >= 21 and mes == 3) or (dia <= 20 and mes == 4):
        return "Áries"
    elif (dia >= 21 and mes == 4) or (dia <= 20 and mes == 5):
        return "Touro"
    elif (dia >= 21 and mes == 5) or (dia <= 20 and mes == 6):
        return "Gêmeos"
    elif (dia >= 21 and mes == 6) or (dia <= 22 and mes == 7):
        return "Câncer"
    elif (dia >= 23 and mes == 7) or (dia <= 22 and mes == 8):
        return "Leão"
    elif (dia >= 23 and mes == 8) or (dia <= 22 and mes == 9):
        return "Virgem"
    elif (dia >= 23 and mes == 9) or (dia <= 22 and mes == 10):
        return "Libra"
    elif (dia >= 23 and mes == 10) or (dia <= 21 and mes == 11):
        return "Escorpião"
    elif (dia >= 22 and mes == 11) or (dia <= 21 and mes == 12):
        return "Sagitário"
    elif (dia >= 22 and mes == 12) or (dia <= 20 and mes == 1):
        return "Capricórnio"
    elif (dia >= 21 and mes == 1) or (dia <= 18 and mes == 2):
        return "Aquário"
    elif (dia >= 19 and mes == 2) or (dia <= 20 and mes == 3):
        return "Peixes"
    else:
        return "Data inválida!"

def main():
    print("=== Verificador de Signo ===")
    
    data_str = input("Digite sua data de nascimento (dd/mm/aaaa): ")

    try:
        data = datetime.strptime(data_str, "%d/%m/%Y")
        dia = data.day
        mes = data.month

        signo = descobrir_signo(dia, mes)
        print(f"\nSeu signo é: {signo}")

    except ValueError:
        print("Formato inválido! Use dd/mm/aaaa.")

if __name__ == "__main__":
    main()

