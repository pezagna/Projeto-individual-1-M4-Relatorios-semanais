import pandas as pd


Relatorio_Semanal = {'Dia': ['Segunda-Feira','Terça-Feira','Quarta-Feira','Quinta-Feira','Sexta-Feira','Sábado','Domingo'] ,
                'Limpeza' : [100 , 0 , 100, 0 , 100 , 100 , 0] ,
                'Comida' : [221.60 , 375.31 , 412 , 495.20 , 411.53 , 245 , 164] ,
                'Transporte' : [150 , 100 , 125 , 300 , 275 , 525 , 75] ,
                'Outros' : [0 , 0 , 2310, 500 , 0 , 0 ,820]}
Relatorio_Semanal_DF = pd.DataFrame(Relatorio_Semanal) 

# Definindo a porcentagem de impostos
imposto = 0.07

# Criar a tabela Ganhos e adicionar dados
ganhos = [2200, 2420.50, 3391, 5322, 4898.50, 4200, 3893]
Relatorio_Semanal_DF['Ganhos'] = ganhos
print(Relatorio_Semanal_DF)

# Exibir a subtração de impostos dos Ganhos Diários, que nesta semana foi de 7%;
Ganhos_Diarios = (Relatorio_Semanal_DF['Ganhos'] * 0.93).round(2)
print("\nResultado dos Ganhos Diarios subtraindo os impostos de 7%")
print(Ganhos_Diarios)

######################################################################################################################
# Calcular a soma total dos ganhos
total_ganhos = Relatorio_Semanal_DF['Ganhos'].sum()
print("\nResultado da soma total dos ganhos: R$",round(total_ganhos,2))

#######################################################################################################################
# Calcular a média semanal dos ganhos
media_ganhos = (Relatorio_Semanal_DF['Ganhos']).mean()
print("\nResultado da Média semanal dos ganhos:  R$", round (media_ganhos,2),"nesta semana.")

#######################################################################################################################
# Exibir soma total das despesas por categorias específicas
soma_despesas = Relatorio_Semanal_DF[['Limpeza', 'Comida', 'Transporte', 'Outros']].sum()
print("\nResultados da soma total das despesas por categoria:")
print(soma_despesas)


#######################################################################################################################
# Calculando a média semanal de todas as despesas
media_despesas_semanal = Relatorio_Semanal_DF[['Limpeza', 'Comida', 'Transporte', 'Outros']].mean().round(2)
print("\nMédia semanal de todas as despesas:")
print(media_despesas_semanal)


#######################################################################################################################
# Calculando o Lucro_Diario
# Exibindo o Lucro_Diario
Relatorio_Semanal_DF['Lucro_Diario'] = Relatorio_Semanal_DF['Ganhos']*0.93 - Relatorio_Semanal_DF[['Limpeza', 'Comida', 'Transporte', 'Outros']].sum(axis=1)
print("\nExibindo Lucro_Diario para informar o dia mais lucrativo:\n",round(Relatorio_Semanal_DF,2)[['Dia', 'Lucro_Diario']])

########################################################################################################################
# Exibindo o lucro total da semana com desconto do imposto de 7%
lucro_diario = Relatorio_Semanal_DF['Lucro_Diario']
lucro_total = lucro_diario.sum()
print('\nResultado para o lucro total da semana:', round(lucro_total,2))


# Exibir o relatorio completo
print(Relatorio_Semanal_DF)
