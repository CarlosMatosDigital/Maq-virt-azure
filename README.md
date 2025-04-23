# Maq-virt-azure
Processo de criação e configuração de uma máquina virtual na plataforma Microsoft Azure.
O curso disponibilizado pela plataforma DIO ensina que as máquinas virtuais (VM) do Azure podem ser criadas por meio do Portal do Azure.
Todo o método de criação fornece uma interface de usuário baseada em navegador para criar as VMS seus recursos relacionados.
Os seguintes passos vão mostrar como usar o portal do Azure para implantar uma máquina virtual (VM) no Azure que executa o Windows Server 2020 Datacenter e,  para ver a VM em ação, será necessária a habilitação do protocolo RDP na VM e instalação do servidor Web do IIS.
Para quem não possui uma assinatura do Azure, faz-se necessária a criação de uma conta gratuita antes de começar.
É importante que se saiba que as etapas descritas se tratam de passos básicos através de informações repassadas através da plataforma do curso, sendo uma forma didática de ensino e que não se destina às implantações em um ambiente de produção, já que este necessita de dados mais sensíveis, precisos e focados em um resultado para um ambiente empresarial.
Após entrar no portal Azure siga os seguintes passos:
Na parte de pesquisas digite: máquinas virtuais.
E na opção Serviços, selecione Máquinas virtuais.
Na página Máquinas virtuais, deverá clicar em Criar e selecionar a opção de Máquina virtual do Azure. 
Logo em seguida a página Criar uma máquina virtual é aberta.
Na opção Detalhes da instância, deverá inserir myVM no Nome da máquina virtual e a escolha do Windows Server 2020 Datacenter: Azure Edition - x64 Gen 2.
Na opção Conta de administrador, deverá ser fornecido um nome de usuário e uma senha, que deverá ter, no mínimo 12 caracteres, além de ter que atender aos requisitos de complexidade de segurança que já são determinados.
Na opção de Regras de porta de entrada, escolha Permitir portas selecionadas e, em seguida, selecione RDP (3389) e HTTP (80), que estão na lista suspensa.
Os padrões restantes podem ser deixados e, em seguida, deve-se selecionar o botão Examinar + criar, que está localizado na parte inferior da página.
Ao término da validação, selecione o botão Criar, na parte inferior da página.Ao término da conclusão da implantação, selecione Ir para o recurso.
Finalizando todos os passos, para se conectar à VM, faz-se necessária a inicialização de uma conexão da área de trabalho remota para a máquina virtual.
