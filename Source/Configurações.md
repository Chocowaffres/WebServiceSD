# Setup IIS
 1. Painel de controlo -> Ativar e desativar funcionalidades -> Check Serviços de Informação e Internet
 2. Abrir o Gestor de Serviços de Informação e Internet -> Expandir servidor -> Expandir Sites
 3. Action no Default Web Site -> Adicionar Diretório Virtual
 4. Colocar o Alias que vai user para o URL e a pasta root para o virtual host
 5. Clicar Ligar como... -> Selecionar Utilizador específico -> Definir -> Introduzir utilizador do computador
 6. Clicar Definições de Teste... -> Verificar que está tudo verde
 7. Duplo clique na diretoria virtual criada -> Coluna lado direito -> Procurar *:80
 8. Colocar WebService na diretoria pretendida 
 9. HTTP 404.3 : 1. Painel de controlo -> Ativar e desativar funcionalidades
				 2. Expandir Serviços de Informação de Internet -> Expandir Serviços da World Wide Web -> Expandir Funcionalidades de desenvolvimento de aplicações
				 3. Selecionar .NET Extensibilty 3.5 e 4.5, ASP, ASP.NET 3.5 e 4.5, Extensões ISAPI e Filtros ISAPI

# Open firewall ports
  1. Painel de controlo -> Firewall -> Definições Avançadas
  2. Coluna lado esquerdo -> Regras de Entrada -> Action -> Nova Regra
  3. Tipo de Regra = Predefinida -> Serviços da World Wide Web (HTTP) -> Seguinte
    Regras Predefinidas -> Selecionar a opção -> Seguinte
    Ação -> Permitir a ligação
  4. Tipo de Regra = Predefinida -> Serviços da World Wide Web Protegidos (HTTPS) -> Seguinte
    Regras Predefinidas -> Selecionar a opção -> Seguinte
    Ação -> Permitir a ligação

# Configure HTTPS on IIS

  1. Gestor de Serviços de Informação Internet (IIS);
  2. Botão do lado direito no Default Web Site;
  3. Editar enlaces;
  4. Adicionar e escolher "https";
  5. Escolher Certificado SSL : IIS Express Development Certificate;
  6. Ir às funcionalidades do site e selecionar definições de ssl;
  7. Selecionar Exigir SSL e deixar ignorar.