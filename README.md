# PetVida Clínica — Sistema de Agendamento e Prontuário

Protótipo funcional de um **sistema web (dashboard)** para a **Clínica PetVida & Estética Animal**, desenvolvido para a disciplina *Design Profissional — Produção de Portfólio & Desenvolvimento Empresarial* (Estudo de Caso 5, Prof. Sedenilso Antonio Machado).

## 1. A PetVida
Clínica veterinária e centro de estética pet de bairro, fundada pelo Dr. Gabriel Santos e pela Dra. Camila Paes. Oferece consultas, vacinação, cirurgias de pequeno porte e banho e tosa. Equipe: 2 sócios, 2 veterinários plantonistas, 3 tosadores e 2 recepcionistas.

## 2. Problema identificado (briefing)
Todo o agendamento é feito em **agenda de papel** na recepção. Com mais de 30 banhos por dia e consultas sobrepostas, surgiram:

| Dor do cliente | Consequência |
|---|---|
| Choques de horários | Atrasos e insatisfação dos tutores |
| Tutores esquecem banho/vacina | Lacunas na agenda não preenchidas a tempo |
| Histórico médico em pastas físicas | Recepção perde minutos procurando fichas |
| Sem lembretes de retorno preventivo | Perda de receita e baixa previsibilidade de caixa |

**Oportunidade:** integrar o cuidado estético ao histórico de saúde do animal, dando praticidade ao tutor e previsibilidade à clínica (diferencial frente às redes de pet shops).

## 3. Solução e justificativa (App × Site × Sistema)
Foi escolhido um **sistema/dashboard web** de uso interno.

- **Por que não um app móvel?** A dor principal está *dentro* da clínica (recepção, veterinários e tosadores). Um app exigiria instalação pelos tutores e publicação em lojas, o que é inviável para o prazo e para um computador comum.
- **Por que não um site institucional?** Divulga a clínica, mas não resolve conflito de horários nem histórico.
- **Por que um sistema web?** Roda em qualquer navegador, sem instalação e sem custo, e atende recepção, veterinários e tosadores na mesma tela. O contato com o tutor acontece pelos **lembretes** (simulados como mensagem de WhatsApp).

**Público-alvo:** recepcionistas (agenda e cadastros), veterinários (prontuário), tosadores (agenda e observações) e sócios (dashboard). Tutores são atendidos indiretamente, via lembretes.

## 4. Funcionalidades → dor que resolve
| Funcionalidade | Dor resolvida |
|---|---|
| **Agenda única** (veterinários + tosadores) com bloqueio de conflito de profissional e de pet | Choques de horários |
| Células “+ livre” destacadas e contador de horários livres | Lacunas na agenda |
| **Lembretes** de vacinas e retornos (até 30 dias ou atrasados) com mensagem pronta | Esquecimento e perda de receita |
| **Prontuário** com linha do tempo de consultas, vacinas **e banhos** | Histórico demorado; integração saúde + estética |
| Cadastro de tutores e pets | Organização dos dados |
| **Dashboard** (ocupação, confirmações, lacunas, lembretes) | Previsibilidade para a clínica |
| Status do atendimento (Agendado → Confirmado → Concluído) | Situação dos agendamentos |
| Tela de equipe | Gestão dos profissionais |

Regra extra: consultas/vacinas/cirurgias só podem ser marcadas com veterinários, e banho/tosa com tosadores.

## 5. Tecnologias
HTML5, CSS3 (responsivo) e JavaScript puro. Dados fictícios em `js/data.js`, salvos no `localStorage` do navegador. **Sem backend, sem banco, sem dependências.**

## 6. Arquitetura e estrutura de pastas
Aplicação de página única (SPA) simples: `data.js` fornece os dados, `app.js` guarda o estado, renderiza cada tela e liga os eventos; a navegação usa o `#hash` da URL.

```
petvida-clinica/
├── index.html        # estrutura e menu
├── css/style.css     # identidade visual (verde-saúde + laranja)
├── js/data.js        # dados de demonstração
├── js/app.js         # telas e regras de negócio
├── docs/             # prints das telas (veja seção 7)
├── .gitignore
├── LICENSE
└── README.md
```

## 7. Protótipos / telas
Telas: **Dashboard, Agenda, Tutores e Pets, Prontuário, Lembretes e Equipe**.
Salve os prints em `docs/` (ex.: `docs/dashboard.png`, `docs/agenda.png`) e referencie aqui com `![Agenda](docs/agenda.png)`.

## 8. Instalação e execução
Não há instalação. Opções:
1. Baixe/clone o repositório e abra `index.html` no navegador; **ou**
2. `python -m http.server 8000` na pasta e acesse `http://localhost:8000`; **ou**
3. Publique pelo **GitHub Pages** (Settings → Pages → branch `main`, pasta `/root`).

O botão **↺ Restaurar demo** devolve os dados originais.

## 9. Segurança
Nenhuma senha, token ou chave de API existe no código ou no histórico. Todos os dados são fictícios. Textos digitados pelo usuário são escapados antes de ir para a tela (evita injeção de HTML). Em uma versão real seriam necessários login, backend e banco com controle de acesso (LGPD).

## 10. Licença
Distribuído sob a licença [MIT](LICENSE).
