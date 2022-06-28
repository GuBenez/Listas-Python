lista = []
dados = []
totnome = 0
pesopesado = []
pesoleve = []
while True:
    lista.append(str(input("Digite o nome a ser guardado: ")))
    lista.append(float(input("Digite o peso: ")))
    totnome += 1
    dados.append(lista[:])
    lista.clear()
    perg = str(input("Deseja continuar: [S/N] ")).strip().upper()[0]
    if perg == "N":
        break
for p in dados:
    if p[1] > 70:
        pesopesado.append(p[0])
    if p[1] < 70:
        pesoleve.append(p[0])

print("A lista dos mais pesados é: {}".format(pesopesado))
print("A lista com os mais leves é: {}".format(pesoleve))
print("A lista digitada foi : {}".format(dados))
print("O total de pessoas inseridas na lista foi de: {} pessoas".format(totnome))