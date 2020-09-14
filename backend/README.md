# Recuperação de senha

**RF**
- [x] O usuário deve poder recuperar sua senha informando o seu e-mail;
- [x] O usuário deve receber um e-mail com as instruções de recuperação de senha;
- [x] O usuário deve poder resetar sua senha;

**RNF**
- [x] Utilizar Ethereal para testar envios em ambiente de desenvolvimento;
- [] Utilizar o Amazon SES para envios em produção;
- [] O envio de e-mails deve acontecer em segundo plano (background jobs);

**RN**
- [x] O link enviado por e-mail para resetar a senha, deve expirar em 2 horas;
- [x] O usuário precisa confirmar a nova senha, ao resetá-la;

# Atualização de perfil

**RF**
- [x] O usuário deve poder atualizar seu nome, e-mail e senha;

**RN**
- [x] O usuário não pode alterar seu e-mail para um e-mail já existente;
- [x] Para atualizar sua senha, o usuário deve informar a senha antiga;
- [x] Para atualizar sua senha, o usuário precisar confirmar a nova senha;

# Painel do prestador

**RF**
- [] O usuário deve poder listar seus agendamentos de um dia específico;
- [] O prestador deve receber uma notificação sempre que houver um novo agendamento;
- [] O prestador deve poder visualizar as notificações não lidas;

**RNF**
- [] Os agendamentos do prestador no dia devem ser armazenados em cache;
- [] As notificações do prestador devem ser armazenadas no MongoDB;
- [] As notificações do prestador devem ser enviadas em tempo real utilizando o Socket IO;

**RN**
- [] A notificação deve ter um status de lida ou não lida;

# Agendamento de serviços

**RF**
- [x] O usuário deve poder listar todos os prestadores de serviço cadastrados;
- [x] O usuário deve poder listar os dias de um mês com pelo menos um horário disponível de um prestardor;
- [x] O usuário deve poder listar os horários disponíveis em um dia específico de um prestador;
- [x] O usuário deve poder realizar um novo agendamento com um prestador;

**RNF**
- [] A listagem de prestadores deve ser armazenada em cache;

**RN**
- [x] Cada agendamento deve durar 1 hora exatamente;
- [x] Os agendamentos devem estar disponíveis entre 8h e às 18h (primeiro 8h, último às 17h)
- [x] O usuário não pode agendar em um horário já ocupado;
- [x] O usuário não pode agendar em um horário que já passou;
- [x] O usuário não pode agendar serviços consigo mesmo;
- [x] O usuário não pode agendar serviços com um prestador que não existe;
