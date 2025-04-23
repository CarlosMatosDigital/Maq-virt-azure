# Maq-virt-azure
Processo de criação e configuração de uma máquina virtual na plataforma Microsoft Azure.
Durante o curso da Dio, foi possível entender que as máquinas virtuais (VM) do Azure podem ser criadas por meio do Portal do Azure.
Todo o método de criação fornece uma interface de usuário baseada em navegador para criar as VMS seus recursos relacionados.
Os seguintes passos vão mostrar como usar o portal do Azure para implantar uma máquina virtual (VM) no Azure que executa o Windows Server 2022 Datacenter e,  para ver a VM em ação, será necessária a habilitação do protocolo RDP na VM e instalação do servidor Web do IIS.
Para quem não possui uma assinatura do Azure, faz-se necessária a criação de uma conta gratuita antes de começar.
É importante que se saiba que as etapas descritas se tratam de passos básicos através de informações repassadas através da plataforma do curso, sendo uma forma didática de ensino e que não se destina às implantações em um ambiente de produção, já que este necessita de dados mais sensíveis, precisos e focados em um resultado para um ambiente empresarial.
Após entrar no portal Azure siga os seguintes passos iniciais:
1. Digite máquinas virtuais na pesquisa.
2. Em Serviços, selecione Máquinas virtuais.
3. Na página Máquinas virtuais, clique em Criar e selecione Máquina virtual do Azure. A página Criar uma máquina virtual é aberta.
4. Em Detalhes da instância, insira myVM no Nome da máquina virtual e escolha Windows Server 2022 Datacenter: Azure Edition - x64 Gen 2 na Imagem. Deixe os outros padrões.
É importante ressaltar que alguns usuários agora verão a opção de criar VMs em várias zonas.
5. Em Conta de administrador, forneça um nome de usuário, como azureuser e uma senha. A senha deve ter no mínimo 12 caracteres e atender a requisitos de complexidade definidos.
6. Em Regras de porta de entrada, escolha Permitir portas selecionadase, em seguida, selecione RDP (3389) e HTTP (80) na lista suspensa.
7. Deixe os padrões restantes e, em seguida, selecione o botão Examinar + criar na parte inferior da página.
8. Após a execução da validação, selecione o botão Criar na parte inferior da página.9. Após a conclusão da implantação, selecione Ir para o recurso.
Para se conectar à VM é necessária a inicialização de uma conexão da área de trabalho remota para a máquina virtual. Estas instruções ensinam a se conectar à sua VM de um computador com Windows. Em um Mac, você precisa de um cliente RDP, como este Cliente de Área de Trabalho Remota da Mac App Store.
Basta seguir os seguintes passos:
1. Selecione Conectar>RDP na página de visão geral de sua máquina virtual.
2. Na guia Conectar-se ao RDP, mantenha as opções padrão para se conectar por endereço IP pela porta 3389 e clique em Baixar arquivo RDP.
3. Abra o arquivo RDP baixado e clique em Conectar quando solicitado.
4. Na janela Segurança do Windows, selecione Mais opções e Usar uma conta diferente. Digite o nome de usuário como localhost\nome de usuário, insira a senha que você criou para a máquina virtual e clique em OK.
5. Você pode receber um aviso do certificado durante o processo de logon. Clique em Sim ou em Continuar para criar a conexão.
Para ver a VM em ação, instale o servidor Web do IIS. Abra um prompt do PowerShell na VM e execute o seguinte comando:
PowerShell
Copiar
Install-WindowsFeature -name Web-Server -IncludeManagementTools
Quando terminar, feche a conexão RDP com a VM.
No portal, selecione a VM e, na visão geral da VM, passe o mouse sobre o endereço IP para mostrar Copiar para a área de transferência. Copie o endereço IP e cole-o em uma guia do navegador.
Quando o grupo de recursos, a máquina virtual e todos os recursos relacionados não forem mais necessários, exclua-os.
1. Na página Visão geral da VM, selecione o link Grupo de recursos.
2. Selecione Excluir grupo de recursos na parte superior da página do grupo de recursos.
3. Uma página abrirá um aviso de que você está prestes a excluir recursos. Digite o nome do grupo de recursos e selecione Excluir para concluir a exclusão dos recursos e do grupo de recursos.
Se a VM ainda for necessária, o Azure fornecerá um recurso de desligamento automático para máquinas virtuais a fim de ajudar a gerenciar custos e garantir que você não seja cobrado por recursos não utilizados.
1. Na seção Operações da VM, selecione a opção Desligamento automático.
2. Uma página será aberta na qual você poderá configurar o tempo para o desligamento automático. Selecione a opção Ativado para habilitar e, em seguida, defina uma hora que seja adequada para você.
3. Depois de definir a hora, selecione Salvar na parte superior para habilitar a configuração de Desligamento automático.
Lembre-se de configurar o fuso horário corretamente para corresponder aos seus requisitos, pois o UTC (Tempo Universal Coordenado) é a configuração padrão na lista suspensa de fuso horário.
Para obter mais informações, confira Desligamento automático.

