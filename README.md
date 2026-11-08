# 🎂 DeliciArte 3D — Da Janinha

**Personalize seu bolo em uma experiência interativa tridimensional.**

O DeliciArte 3D é uma aplicação web de personalização de bolos desenvolvida para a DeliciArte da Janinha. A plataforma permite que o cliente configure seu bolo através de uma interface visual, selecionando tamanho, massa, recheios, cobertura e decoração.

A aplicação utiliza renderização 3D com Three.js para apresentar uma representação visual do bolo, atualizada conforme as opções selecionadas pelo cliente.

O objetivo é tornar o processo de encomenda mais intuitivo, visual e personalizado.

---

## 1. Tecnologias utilizadas

| Tecnologia | Finalidade |
|---|---|
| HTML5 | Estrutura da aplicação |
| CSS3 | Estilização e animações visuais |
| JavaScript | Lógica de funcionamento e interatividade |
| Three.js r128 | Renderização e construção do ambiente 3D |
| GSAP 3.12.2 | Biblioteca de animações |
| Tailwind CSS | Estilização e responsividade |
| OrbitControls | Rotação e navegação do modelo 3D |
| Google Fonts | Tipografia Montserrat e Great Vibes |
| WhatsApp API (wa.me) | Encaminhamento das encomendas |

## 2. Identidade visual

A interface utiliza a identidade visual da DeliciArte da Janinha.

**Paleta principal:**

- Vinho escuro: `#2b0c0e`
- Vinho secundário: `#4a191b`
- Dourado: `#e5a823`
- Rosa: `#ff8ca3`
- Bege: `#EFE3D3`
- Branco: `#FFFFFF`

**Tipografia:**
- Great Vibes: identidade visual da marca.
- Montserrat: textos, controles e informações.

## 3. Funcionalidades da aplicação

### 3.1. Personalização do tamanho

O cliente pode informar o peso desejado para o bolo.

- Peso mínimo: 1 kg.
- Peso máximo: 10 kg.
- Incremento: 0,5 kg.

A escala do modelo 3D é ajustada conforme o tamanho informado.

### 3.2. Seleção de massa

A aplicação disponibiliza cinco opções:

1. Massa branca.
2. Massa mista.
3. Massa de chocolate.
4. Massa de baunilha.
5. Massa amanteigada.

Cada opção possui uma representação visual própria e altera a coloração das camadas de massa no modelo tridimensional.

### 3.3. Seleção de recheios

A quantidade de recheios disponíveis depende do tamanho selecionado.

**Bolos abaixo de 3 kg:**
- Seleção de um recheio.

**Bolos a partir de 3 kg:**
- Seleção de até dois recheios.
- Primeiro recheio: camada inferior.
- Segundo recheio: camada superior.

**Recheios tradicionais:**
- Brigadeiro.
- Brigadeiro Branco.
- Doce de Leite.
- Beijinho.
- Morango.
- Chocolate Amargo.
- Ganache.
- Ninho.
- Limão.
- Maracujá.

**Recheios gourmet:**
- Ninho com Morango.
- Ninho com Nutella.
- Brigadeiro com Morango.

A aplicação utiliza cores associadas aos ingredientes para representar visualmente as camadas de recheio.

### 3.4. Seleção de cobertura

Opções disponíveis:

- Sem cobertura.
- Chantininho.
- Chocolate.
- Brigadeiro.
- Ganache.

A cobertura selecionada modifica a aparência externa do modelo 3D.

### 3.5. Decoração adicional

O cliente pode selecionar:

| Decoração | Valor apresentado |
|---|---:|
| Nenhuma | R$ 0,00 |
| Morango | R$ 7,00 |
| Topo simples | R$ 10,00 |
| Topo personalizado | A combinar |

### 3.6. Personalização do Topper

A interface disponibiliza um campo de texto para informar o tema ou nome que deverá aparecer no topo do bolo.

Exemplos:
- Nome da pessoa.
- Sonic.
- Unicórnio.
- Temas de aniversário.

Também existe um botão para aplicar a personalização.

### 3.7. Ambiente 3D

A visualização tridimensional utiliza Three.js.

Características implementadas:

- Construção do bolo utilizando geometrias cilíndricas.
- Três camadas de massa.
- Duas possíveis camadas de recheio.
- Representação da cobertura externa.
- Prato de apresentação.
- Base de apoio.
- Iluminação ambiente e direcional.
- Sombras.
- Rotação interativa com OrbitControls.
- Atualização do modelo conforme as escolhas do cliente.

### 3.8. Avatar da confeiteira

A aplicação apresenta uma imagem da Janinha dentro do ambiente de personalização.

O avatar possui:
- Posicionamento sobre a área de visualização.
- Balão de fala.
- Animações de interação visual.
- Comportamento responsivo.

O objetivo é aproximar a experiência digital do atendimento humanizado da confeitaria.

## 4. Fluxo de encomenda

O processo de finalização possui duas etapas.

**Etapa 1 — Resumo do pedido**

Ao clicar em Finalizar Pedido, é apresentado um modal contendo:

- Tamanho do bolo.
- Massa selecionada.
- Recheio ou recheios.
- Cobertura.
- Decoração adicional.
- Tema do topper.

O cliente pode voltar para editar as escolhas ou avançar.

**Etapa 2 — Dados do cliente**

O formulário solicita:

- Nome completo.
- Telefone/WhatsApp.
- Data de entrega.
- Horário.
- Endereço de entrega ou retirada.

**Etapa 3 — Envio pelo WhatsApp**

Após o preenchimento, a aplicação prepara uma mensagem formatada com os dados da encomenda e direciona o cliente para o WhatsApp comercial da DeliciArte da Janinha.

Número configurado no código:

`5583988558021`

## 5. Estrutura técnica

A aplicação está concentrada em um arquivo HTML, contendo:

```text
deliciarte-3d/
│
├── index.html
│
└── README.md
```

O arquivo principal contém:

- Estrutura HTML.
- Estilização CSS.
- Importação das bibliotecas externas.
- Configuração da cena Three.js.
- Construção do modelo 3D.
- Gerenciamento do estado das personalizações.
- Eventos de interação.
- Modal de encomenda.
- Integração com WhatsApp.

## 6. Execução

A aplicação pode ser executada em um servidor HTTP local.

Exemplo utilizando Python:

```bash
python3 -m http.server 8000
```

Acessar pelo navegador:

```text
http://localhost:8000
```

**Dependências externas:** as bibliotecas e fontes são carregadas por CDN, sendo necessária conexão com a internet.

## 7. Compatibilidade e desempenho

A aplicação possui configurações voltadas para dispositivos móveis:

- Layout responsivo.
- Ajuste da resolução do renderizador.
- Perfis alternativos de inicialização WebGL.
- Tratamento de perda e restauração do contexto WebGL.
- Controle de resolução para reduzir consumo de GPU.

O sistema também possui tratamento de erros durante a inicialização da renderização 3D.

## 8. Considerações sobre o estado atual

O projeto está em desenvolvimento e possui uma estrutura funcional de personalização e visualização 3D.

Algumas opções da interface ainda não possuem representação tridimensional específica. A decoração adicional e o topper, por exemplo, aparecem na configuração e no resumo, mas ainda precisam de implementação própria na geometria 3D.

O sistema também não possui cálculo automático do preço total do bolo. Os valores exibidos nas opções de decoração são informativos.

O envio pelo WhatsApp depende da conclusão correta do formulário e da integração com o navegador.

## 9. Visão de evolução

O projeto poderá evoluir para uma plataforma completa de encomendas, incluindo:

- Modelos de bolos com diferentes formatos.
- Upload de imagens de referência.
- Decoração 3D com frutas, granulados e outros elementos.
- Topper personalizado renderizado no modelo.
- Visualização detalhada das camadas internas.
- Precificação dinâmica.
- Captura de imagem do bolo personalizado.
- Histórico de encomendas.
- Painel administrativo.
- Integração com banco de dados.
- Integração com automações para gerenciamento dos pedidos.

---

**DeliciArte 3D — Da Janinha**

*Mais do que escolher um bolo, uma experiência de criar o seu próprio doce.*
