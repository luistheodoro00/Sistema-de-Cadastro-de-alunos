# Sistema-de-Cadastro-de-alunos
Um sistema de cadastro de alunos simples

alunos=[]

while True:


    print("Seja bem vindo ao seu sitema de castro de alunos")
    print("="*50)

    print("Para cadastrar aluno digite 1")
    print("Para revomer aluno digite 2")
    print("Para consultar aluno digite 3")
    print("Para mostrar todos os alunos cadastrados digite 4")
    print()
    print("="*50)

    op=int(input("Selecione uma das opções:"))

    if op == 1:


        while True:

            aluno={}
            aluno['nome'] = input("Digite o nome do aluno:")
            aluno['idade'] = int(input("Digite a idade do aluno:"))
            aluno['série'] = str(input("Digite a série do aluno:"))
            print()
            sair=int(input("Para sair digite 0, para continuar cadastradndo digite 1"))

            if sair == 1:

                alunos.append(aluno)
                continue

            if sair == 0:

                alunos.append(aluno)
                break

    if op == 2:

        print(alunos[:])
        qual=str(input("Digite o nome do aluno que deseja apagar:"))

        for aluno in alunos:

            if aluno['nome'] == qual:

                alunos.remove(aluno)
                print("aluno removido com sucesso ")
                break

    if op == 3:

        nome=str(input("Qual o nome do aluno que deseja consultar?"))

        for aluno in alunos:

            if aluno['nome'] == nome:
                for c,v in aluno.items():
                    print(f"{c} : {v} ")


    if op == 4:
        print(alunos)
        break

