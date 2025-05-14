# Configura-o-De-Instancia-BD
Processo de configuração de uma instância de Banco de Dados na plataforma Microsoft Azure
 Acessar o portal - portal.azure.com

2. Criar uma instância do Azure SQL Database
No menu esquerdo digitar “SQL Database” e "SQL databases".

Clicar  em "+ Criar"  "Banco de dados SQL".

Aba: Básico
Preencha os campos principais:

Campo	Valor sugerido
Assinatura ==	Sua assinatura ativa //
Grupo de recursos == Use um existente ou crie um novo //
Nome do banco de dados == a sua escolha // 	
Servidor ==Clique em "Criar novo" //
→ Nome do servidor== a sua escolha // 
→ Região == Brazil South //
→ Autenticação ==	Usuário + senha padrão (use uma senha segura) // 
→ Login == administrador adminsql (ou outra que preferir) // 
→ Senha == usar uma senha forte 
Camada de computação	Uso geral ou Desenvolvimento/Teste (mais barato) // 
Tamanho	Pode clicar em “Configurar banco de dados” e escolher a performance desejada (DTU ou vCore)

Clique em "Próximo: Segurança".

4. Aba: Segurança
Modo de autenticação: mantenha SQL (ou adicione Azure AD se necessário).

Firewall do servidor: adicione o IP público atual para permitir conexão (ou permita todos temporariamente para testes).

Azure Defender para SQL: pode desativar para testes (evita cobrança adicional).

Clique em "Próximo: Rede".

5. Aba: Rede
Conectividade de rede: Acesso público (mais simples para testes).

Para produção: usar rede privada (VNet).

Habilite "Permitir acesso a serviços do Azure" se desejar.

Clique em "Próximo: Configurações adicionais".

6. Aba: Configurações adicionais
Fonte de dados: escolha Banco de dados em branco.

Colação: mantenha padrão (SQL_Latin1_General_CP1_CI_AS) ou ajuste conforme a aplicação.

Backup gerenciado: habilitado por padrão.

Clique em "Próximo: Tags".

7. Aba: Tags (opcional)
Tags ajudam na organização e gerenciamento de custos.

8. Revisar + Criar
O Azure fará a validação.

Clique em "Criar".

9. Acompanhar a implantação
Aguarde o provisionamento do recurso.

Após a conclusão, clique em "Ir para o recurso".
