PetVida Clínica

Projeto de um sistema web para a Clínica PetVida & Estética Animal, desenvolvido para a disciplina Design Profissional — Produção de Portfólio & Desenvolvimento Empresarial, do professor Sedenilso Antonio Machado.

A ideia do projeto é criar um sistema para ajudar a clínica com os agendamentos, cadastro dos animais, prontuários e lembretes.

Sobre o projeto

A PetVida é uma clínica veterinária que também trabalha com banho e tosa.

A clínica possui veterinários, tosadores, recepcionistas e os dois sócios responsáveis pelo local.

O problema encontrado foi que os agendamentos eram feitos em uma agenda de papel. Com muitos atendimentos durante o dia, isso pode acabar causando horários marcados ao mesmo tempo, esquecimento de vacinas e banhos e dificuldade para encontrar o histórico dos animais.

O sistema foi criado para deixar essas informações em um só lugar.

O sistema

O projeto funciona como um dashboard e foi pensado para ser usado pelos funcionários da clínica.

A recepção pode cuidar dos cadastros e dos agendamentos.

Os veterinários conseguem acessar os prontuários dos animais.

Os tosadores conseguem visualizar os horários de banho e tosa.

Os sócios conseguem acompanhar algumas informações da clínica pelo dashboard.

Os tutores não precisam acessar o sistema. Os lembretes simulam o contato da clínica com eles.

Funcionalidades
Dashboard

Mostra algumas informações gerais do sistema, como quantidade de atendimentos, horários livres, confirmações e lembretes.

Agenda

A agenda mostra os horários dos veterinários e tosadores.

Os horários livres ficam destacados para facilitar a visualização.

O sistema também verifica conflitos de horário. Um mesmo profissional não pode ter dois atendimentos no mesmo horário e o mesmo pet também não pode estar em dois atendimentos ao mesmo tempo.

Tutores e Pets

Permite cadastrar e consultar os tutores e seus animais.

Prontuário

Mostra o histórico do animal.

Nele podem aparecer consultas, vacinas e também os registros de banho e tosa.

Lembretes

Mostra vacinas e retornos que estão próximos ou atrasados.

As mensagens são apenas uma simulação de mensagens que poderiam ser enviadas pelo WhatsApp.

Equipe

Mostra os funcionários cadastrados e suas funções.

Regras

O sistema possui algumas regras para os agendamentos.

Consultas, vacinas e cirurgias precisam de um veterinário.

Banho e tosa precisam de um tosador.

Também não é possível colocar dois atendimentos no mesmo horário para o mesmo profissional ou para o mesmo pet.

Os agendamentos possuem os seguintes status:

Agendado
Confirmado
Concluído
Tecnologias

O projeto foi feito usando:

HTML
CSS
JavaScript
LocalStorage

Não foi usado banco de dados ou backend. Os dados usados no projeto são fictícios e ficam salvos no navegador.

Estrutura
petvida-clinica/
├── index.html
├── css/
│   └── style.css
├── js/
│   ├── data.js
│   └── app.js
├── docs/
├── .gitignore
├── LICENSE
└── README.md

O index.html possui a estrutura principal do sistema.

O style.css cuida da parte visual.

O data.js possui os dados usados no projeto.

O app.js controla as telas, eventos e regras do sistema.

A pasta docs possui os prints das telas.

Telas
Dashboard




Agenda




Tutores e Pets




Prontuário




Lembretes




Equipe




Como executar

Não precisa instalar nada para abrir o projeto.

Uma forma simples é baixar o projeto e abrir o arquivo index.html no navegador.

Também pode ser usado um servidor local com Python:

python -m http.server 8000

Depois é só abrir no navegador:

http://localhost:8000

O projeto também pode ser colocado no GitHub Pages.

Restaurar os dados

Os dados ficam salvos no LocalStorage do navegador.

Caso alguma informação seja alterada durante os testes, o botão ↺ Restaurar demo pode ser usado para voltar aos dados originais.

Segurança

Esse projeto foi feito apenas para demonstração e usa dados fictícios.

Não foram colocadas senhas, tokens ou chaves de API no projeto.

Em um sistema real seria necessário ter login, banco de dados e controle de acesso para proteger as informações.

Licença

Projeto disponibilizado usando a licença MIT.