# fun-es
def cumprimentar(nome):
    # Retorna um cumprimento maneiro para o nome passado como argumento em formato de string
    return f"opa, {nome}, que bom que você veio!"

def negar(nome):
    # Retorna uma negação educada para o nome passado como argumento em formato de string
    return f"opa, {nome}, você não está na lista."

def chamar(nome):
    # Retorna um chamado para o nome passado como argumento em formato de string
    return f"opa, {nome}, estou esperando você."

def pode_entrar(nome, lista_convidados):
    # Retorna True se o nome está presente na lista de convidados, caso contrário, retorna False.
    for convidado in lista_convidados:
        if nome == convidado:
            return True
        return False

def receber_convidados(lista_convidados, lista_vieram):
    # Para cada convidado na lista de convidados:
        # Se o convidado pode entrar, cumprimente-o.
        # Se o convidado não pode entrar, negue a entrada.
        for nome in lista_vieram:
            if pode_entrar (lista_convidados=lista_convidados, nome=nome) == True:
                print( cumprimentar(nome) )
            if pode_entrar(lista_convidados, lista_vieram) == False:
                print( negar (nome) )
        

def chamar_faltantes(lista_convidados, lista_vieram ):
    # Para cada convidado na lista de convidados:
        # Se o convidado não veio, chame-o.
        for convidado in lista_vieram:
             if convidado in lista_vieram:
                   print(chamar(convidado))

        
def main():
    lista_convidados = ["Maria", "Ana", "João", "Pedro", "José"]
    lista_vieram = ["João", "Ana", "Maria", "Caio O Penetra"]
    receber_convidados(lista_convidados, lista_vieram)
    chamar_faltantes(lista_convidados, lista_vieram)

if __name__ == '__main__':
    main()
