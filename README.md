Simulação de Ondas Whistler/Chorus
Dispersão a Frio e Partícula-Teste com Python

Autores:

Mauricio Alejandro González Lucero Villalba

Gustavo Schulte

Luis Monteiro

Orientador:

Gustavo do Amaral Valdiviesso

📘 Descrição Geral

Este repositório contém uma simulação didática de ondas whistler/chorus na magnetosfera terrestre, abordando dois fenômenos fundamentais:

Dispersão fria do modo R (whistler), obtendo a relação 
𝑘
(
𝜔
)
k(ω).

Interação onda–partícula, simulando o movimento de um elétron sob um campo magnético uniforme 
𝐵
0
B
0
	​

 e um campo elétrico oscilante representando uma onda eletromagnética.

O projeto integra conceitos de física de plasmas, ressonância ciclotrônica e programação científica, utilizando Python com as bibliotecas NumPy, Matplotlib, FFT e o método de integração Runge–Kutta de 4ª ordem (RK4).

🔬 Contexto Físico

Na magnetosfera terrestre, elétrons aprisionados nos cinturões de radiação realizam movimento helicoidal em torno das linhas do campo magnético com frequência ciclotrônica:

Ω
𝑒
=
𝑒
𝐵
0
𝑚
𝑒
.
Ω
e
	​

=
m
e
	​

eB
0
	​

	​

.

Quando uma onda whistler possui frequência próxima dessa frequência natural, ocorre a ressonância ciclotrônica, permitindo que a onda transfira energia para o elétron. Esse mecanismo é essencial para processos de aceleração e para a geração das ondas chorus observadas na magnetosfera.

A simulação permite visualizar:

regiões de propagação permitidas pela dispersão (onde 
𝑛
2
(
𝜔
)
≥
0
n
2
(ω)≥0);

órbitas da partícula com e sem onda;

ganho de energia em função da frequência da onda;

robustez da ressonância ao variar a fase inicial da onda.

🧮 Modelagem Matemática
📌 Dispersão fria (modo R)
𝑛
2
(
𝜔
)
=
1
−
𝜔
𝑝
𝑒
2
𝜔
(
𝜔
−
Ω
𝑒
)
,
𝑘
(
𝜔
)
=
𝑛
(
𝜔
)
 
𝜔
𝑐
.
n
2
(ω)=1−
ω(ω−Ω
e
	​

)
ω
pe
2
	​

	​

,k(ω)=
c
n(ω)ω
	​

.
📌 Movimento da partícula-teste
𝑥
˙
=
𝑣
𝑥
,
𝑦
˙
=
𝑣
𝑦
,
x
˙
=v
x
	​

,
y
˙
	​

=v
y
	​

,
𝑚
𝑣
˙
=
𝑞
(
𝐸
+
𝑣
×
𝐵
0
)
,
m
v
˙
=q(E+v×B
0
	​

),

com:

𝐵
0
=
𝐵
0
𝑧
^
,
𝐸
=
𝐸
0
cos
⁡
(
𝑘
𝑥
−
𝜔
𝑡
+
𝜙
0
)
𝑥
^
.
B
0
	​

=B
0
	​

z
^
,E=E
0
	​

cos(kx−ωt+ϕ
0
	​

)
x
^
.

A integração temporal é realizada com Runge–Kutta de 4ª ordem (RK4).

🎯 Objetivos do Projeto

Implementar e visualizar a dispersão fria do modo whistler.

Integrar as equações de movimento de um elétron em campos prescritos.

Detectar e analisar a ressonância ciclotrônica.

Aplicar ferramentas adicionais como FFT, varredura em parâmetros e mini-Vlasov.

Produzir gráficos e animações para interpretação física clara.

📁 Estrutura do Repositório
├── Projeto_Computacao_Cientifica.ipynb   # Notebook principal do projeto
├── config.json (opcional)                 # Arquivo para parâmetros externos
├── animations/                            # MP4 gerados pelas animações
├── README.md                               # Documento atual
└── LICENSE                                 # Licença MIT

▶️ Como Executar
1. Instale as dependências:
pip install numpy matplotlib

2. Abra o notebook no Google Colab ou Jupyter.
3. Execute célula por célula:

dispersão 
𝑘
(
𝜔
)
k(ω);

simulação da partícula;

varredura 
𝐾
𝑓
(
𝜔
)
K
f
	​

(ω);

FFT do campo elétrico;

heatmaps;

mini-Vlasov;

animações.

As células estão numeradas e comentadas para facilitar o uso.

📊 Resultados Obtidos

Curva de dispersão: identifica as regiões permitidas e proibidas para ondas whistler.

Órbita do elétron: movimento helicoidal modulado pelo campo elétrico.

Pico de ressonância: máximo de energia quando 
𝜔
≈
∣
Ω
𝑒
∣
ω≈∣Ω
e
	​

∣.

Heatmap 
𝐾
𝑓
(
𝜔
,
𝜙
0
)
K
f
	​

(ω,ϕ
0
	​

): mostra robustez do acoplamento onda–partícula.

FFT: confirma o conteúdo espectral da onda.

Mini-Vlasov: permite visualizar deformações de uma distribuição no espaço de fase.

🧠 Arquitetura Computacional

Integração temporal estável com RK4.

Uso de máscaras booleanas para regiões não propagantes.

Varreduras otimizadas em frequência e fase.

Conservação de energia verificada numericamente.

Animações exportadas em MP4 para evitar limites do Colab.

🏁 Conclusões

O projeto demonstra de forma clara a interação onda–partícula em plasmas magnetizados e o papel central da ressonância ciclotrônica.
Além de revelar fenômenos físicos fundamentais, o trabalho desenvolve habilidades práticas em modelagem, simulação, análise numérica e visualização científica — todas essenciais na formação moderna em física.

📚 Referências

As referências completas encontram-se no arquivo bibliografia.tex do projeto, incluindo:

Stix (1992) — Waves in Plasmas

Omura et al. (2008) — Geração de ondas chorus

Helliwell (1965) — Fenômenos whistler clássicos

Chen (2016) — Introdução à física de plasmas

Hunter (2007) — Matplotlib

📜 Licença

Este projeto está licenciado sob a MIT License.
Você é livre para usar, modificar e distribuir citando os autores originais.
