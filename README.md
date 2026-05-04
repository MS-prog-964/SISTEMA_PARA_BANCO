class ContaCorrente:
    def __init__(self, titular, numero_conta, saldo):
        self.titular = titular
        self.numero_conta = numero_conta
        self.saldo = saldo
    def depositar(self):
        valor = float(input("Digite o valor: "))
        self.saldo = self.saldo + valor
        print(f"Valor adicionado a conta {self.numero_conta}")
    def sacar(self, valor):
        if valor <= self.saldo:
            self.saldo = self.saldo - valor
            print("Seu saque foi realizado com sucesso!")
        else: 
            print("Saldo insuficiente")  
    def pix(self, valor, conta_destino):
        valor = float(input("Digite o valor: "))
        self.saldo = self.saldo - valor
        print(f"Transferência bem sucedida para {conta_destino.numero_conta}")
        conta_destino.saldo = conta_destino.saldo + valor
    def ver_saldo(self):
        print(f"---SALDO DA CONTA {self.numero_conta}")
        print(f"titular: {self.titular}")
        print(f"Saldo atual: R$ {self.saldo}")   
titular1 = input("Nome do titular: ")
numero_da_conta = input("Número da conta:  ")
saldo_inicial = float(input("Saldo: R$ "))
conta1 = ContaCorrente(titular1, numero_da_conta, saldo_inicial)

conta1.depositar()
valor_saque = float(input("Valor do saque: "))
conta1.sacar(valor_saque)

titular2 = input("Nome do titular: ")
numero_da_conta = input("Número da conta: ")
saldo_inicial = float(input("Saldo: "))
conta2 = ContaCorrente(titular2, numero_da_conta, saldo_inicial)
conta1.pix(0, conta2)
print("\n--- SALDO FINAL ---")
conta1.ver_saldo()
conta2.ver_saldo()

    
