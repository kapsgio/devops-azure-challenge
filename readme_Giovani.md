1. Configurar um servidor na Azure, executando uma versão Ubuntu LTS.

Acessar o Portal Azure e autenticar com a conta, acessar Virtual machines e selecionar "Create Virtual Machine", seguir os passos abaixo:

• Região - (US) East US 2 (eastus2) // US porque é mais barato e rápido (caso não haja necessidade regulatória de os dados do cliente precisarem estar no Brasil)
• Resource Group - rg-ubuntu // Um novo Resource Group onde todos os componentes serão instalados, facilita administração
• Availability Zone habilitade para ter uma redundância na VM
• Imagem - Ubuntu Server 22.04 LTS // mais recente
• Tamanho - Standard_B2s - 2vcpus, 4GiB memory // suficiente para o servidor com nginx, já que não ter parte gráfica
• Tipo de conexão - ssh com username nginxadm
• Public Key - gerada uma nova
• Liberar porta SSH (22), posteriormente habilitar somente para o meu IP, e liberar outro • IP caso alguém precise acessar
• OS disk 30 Gib Premium SSD
• Vnet - Uma nova vnet com pelo menos 2 subnets
• Máquina com IP público para eu conseguir acessá-la (opção para remover o IP público é criar um servidor Bastion e utilizado como ponte de acesso)
• Auto-shutdown desabilitado
• Tag - Nome = Servidor Ubuntu nginx
 Review and Create. (fiz e funcionou!)

Após máquina criada ir em Networking > Networking Settings e selecionar somente o meu IP para conectar à VM, existem diversas maneiras de conectar, inclusive de dentro do powershell Windows, liberando permissão de acesso a chave.pem

2. Instalar e configurar qualquer software que você recomendaria em uma configuração de servidor padrão sob as perspectivas de segurança, desempenho, backup e monitorização.

• sudo apt update // atualizar por questões de segurança

• sudo apt install htop // uma versão mais dinâmica do top, quando o usuário está conectado ao servidor consegue verificar métricas de uso de CPU, memória, serviços executados, etc.

• O backup center seria o lugar para fazer o backup da máquina, automático ou manual

3. Instalar e configurar o nginx para servir uma página web HTML estática.

sudo apt install nginx
sudo systemctl start nginx
sudo systemctl enable nginx


4. Utilizar ferramentas de automatização como Ansible e/ou Terraform.

Não tenho domínio dessa parte, IAC não é meu forte, conheço o ARM e arquivos no formato .Json, porém nunca criei um arquivo .Json do zero, apenas testes em laboratórios e aulas, detalhar todas as informações necessárias para subir uma VM no Azure requer mais domínio, abaixo o que consegui criar:

    "parameters": {
      "resourceGroupName": {
        "type": "string",
        "defaultValue": "rg-ubuntu"},
      "location": {
        "type": "string",
        "defaultValue": "eastus2"},
      "vmName": {
        "type": "string",
        "defaultValue": "vm-ubuntu"},
      "adminUsername": {
        "type": "string",
        "defaultValue": "azureuser"},
      "nicName": {
        "type": "string",
        "defaultValue": "nic-ubuntu"},
      "publicIpName": {
        "type": "string",
        "defaultValue": "publicip-ubuntu"},
      "vnetName": {
        "type": "string",
        "defaultValue": "vnet-ubuntu"}
	},

"resources":... // não me recordo como criar os recursos

Para executar basta ir no CLI do portal do Azure, ou pelo Powershell com os módulos de Az instalados.

Ao criar uma VM pelo portal (seja ela Windows, Ubuntu ou qualquer outra) é possível exportar o ARM de criação dela. Automation > Export template. (Isso eu consegui fazer!)

2. Utilizando uma linguagem de script à sua escolha, construa um projeto (servido através do nginx) que possa relatar estatísticas operacionais básicas sob a forma de um objeto JSON.

Minhas habilidades de script para estas estatísticas não são o suficiente, não consigo criar isso do zero, mas estaria disposto a aprender um pouco mais em .json, atualmente minhas habilidades de script são com navegação em Ubuntu e Centos, Windows Powershell e Visual Studio Code (fazendo conexões e acessando o Microsoft Azure, Microsoft 365, Dynamics e outros serviços).


Part 3 – Continuous Delivery

Também não é o meu forte, apesar de eu gostar e desenhos de arquitetura com topologia de redes conexão entre serviços, o CI/CD é mais pro lado de desenvolvedor e eu, como arquiteto não tenho grandes habilidades de desenvolvimento, meu forte é gerenciamento/administração/planejamento, parte analítica tendo domínio de várias ferramentas do Azure, mas pouco relacionado à desenvolvimento
Estarei fazendo algum curso de Devops e Github em breve..
tempo gasto no teste, aproximadamente 2 horas.
