import pandas as pd

# Variables for Gematria
#word = 'טולידאנו' #Sample hebrew's lastname, input your target

word = 'טולידאנו'
gematria_count = len(word)

# Functions for Gematria
def suma_de_digitos(numero):
    numero = str(numero)
    suma = 0
    for i in numero:
        suma += int(i)
    return suma

# dataset AlefBet
#initialize a dataframe
alephbet = pd.DataFrame(
    [[1, 400,   1, 111,  1,   1, 'Aleph', 'א'],
     [2, 300,   2, 412,  2,   2, 'Bet', 'ב'],
     [3, 200,   3,  83,  3,   3, 'Gimel', 'ג'],
     [4, 100,   4, 434,  4,   4, 'Daleth', 'ד'],
     [5,  90,   5,   6,  5,   5, 'Heh', 'ה'],
     [6,  80,   6,  12,  6,   6, 'Vav', 'ו'],
     [7,  70,   7,  67,  7,   7, 'Zayin', 'ז'],
     [8,  60,   8, 418,  8,   8, 'Het', 'ח'],
     [9,  50,   9, 419,  9,   9, 'Tet', 'ט'],
     [1,  40,  10,  20, 10,  10, 'Yud', 'י'],
     [2,  30,  20, 100, 11,  20, 'Kaf', 'כ'],
     [3,  20,  30,  74, 12,  30, 'Lamed', 'ל'],
     [4,  10,  40,  80, 13,  40, 'Mem', 'מ'],
     [5,   9,  50, 106, 14,  50, 'Nun', 'נ'],
     [6,   8,  60, 120, 15,  60, 'Samech', 'ס'],
     [7,   7,  70, 130, 16,  70, 'Ayin', 'ע'],
     [8,   6,  80,  81, 17,  80, 'Peh', 'פ'],
     [9,   5,  90, 104, 18,  90, 'Tzady', 'צ'],
     [1,   4, 100, 186, 19, 100, 'Koof', 'ק'],
     [2,   3, 200, 510, 20, 200, 'Reish', 'ר'],
     [3,   2, 300, 350, 21, 300, 'Shin', 'ש'],
     [4,   1, 400, 406, 22, 400, 'Taf', 'ת'],
     [2,  30, 500, 100, 23,  20, 'Kaf(final)', 'ך'],
     [4,  10, 600,  80, 24,  40, 'Mem(final)', 'ם'],
     [5,   9, 700, 106, 25,  50, 'Nun(final)', 'ן'],
     [8,   6, 800,  81, 26,  80, 'Peh(final)', 'ף'],
     [9,   5, 900, 104, 27,  90, 'Tzady(final)', 'ץ']],
    columns=['Katan','Atbash','Large','Shemi', 'Ordinal','Decimal','Hebrew','Glyph'])

# Gematria delivery
glyph = (alephbet.loc[alephbet['Ordinal'] == gematria_count, "Glyph"]).item()
print('| Word =', word)
print('| Gematria Count =', gematria_count, glyph)
methods = ['Ordinal', 'Decimal', 'Shemi', 'Large', 'Atbash', 'Katan']
for method in methods:
        value = total = 0
        for letter in word:
            value = (alephbet.loc[alephbet['Glyph'] == letter, method]).item()
            total = total + value
        else:  
            numero = int(total)
            while numero > 9:
                numero = suma_de_digitos(numero)
        print('| Gematria', method, total, 'Single', numero)
