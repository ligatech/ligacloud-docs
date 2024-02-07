Experiência de Usuário
===============================

Nesta página, descrevemos a hierarquia de recursos do Google Cloud e os recursos que podem ser gerenciados com o Resource Manager.

O objetivo da hierarquia de recursos do Google Cloud é duplo:

Fornecer uma hierarquia de propriedade, que vincula o ciclo de vida de um recurso ao próprio pai imediato na hierarquia.

Fornecer pontos de conexão e herança para controle de acesso e políticas da organização.

Metaforicamente falando, a hierarquia de recursos do Google Cloud se parece com o sistema de arquivos encontrado em sistemas operacionais tradicionais na forma de organizar e gerenciar entidades hierarquicamente. Geralmente, cada recurso tem exatamente um pai. Essa organização hierárquica de recursos permite definir políticas de controle de acesso e configurações em um recurso pai, e as configurações de políticas e do Identity and Access Management (IAM) são herdadas pelos filhos.

.. note::
    **Observação**: se você estiver começando a usar o Google Cloud, configure sua hierarquia de recursos e conceda acesso inicial como parte do processo de configuração do Google Cloud.


https://cloud.google.com/resource-manager/docs/cloud-platform-resource-hierarchy?hl=pt-br#folders

Hierarquia de recursos do Google Cloud em detalhes
---------------------------------------------------

Persons
Organizations

Producer
    - Tenants
    - Projects
    - Service

Os recursos do Google Cloud são organizados hierarquicamente. Todos os recursos, exceto o mais alto de uma hierarquia, têm exatamente um pai. No nível mais baixo, os recursos de serviço são os componentes fundamentais que compõem todos os serviços do Google Cloud. Exemplos de recursos de serviço incluem máquinas virtuais (VMs) do Compute Engine, tópicos do Pub/Sub, buckets do Cloud Storage, instâncias do App Engine. Todos esses recursos de nível inferior têm recursos de projeto como pais, que representam o primeiro mecanismo de agrupamento da hierarquia de recursos do Google Cloud.

Todos os usuários, incluindo usuários de teste gratuito, usuários de nível gratuito e clientes do Google Workspace e do Cloud Identity, podem criar recursos do projeto. Os usuários do Programa gratuito do Google Cloud só podem criar recursos de projeto e de serviço dentro dos projetos. Os recursos do projeto podem estar no topo da hierarquia, mas somente se criados por um usuário de avaliação gratuita ou um usuário de nível gratuito. Os clientes do Google Workspace e do Cloud Identity têm acesso a recursos extras da hierarquia de recursos do Google Cloud, como recursos de organização e pasta. Saiba mais na visão geral do Cloud Identity. Os projetos no topo da hierarquia não têm recursos pais, mas podem ser migrados para um recurso da organização depois que ele tiver sido criado para o domínio. Para mais detalhes sobre como migrar recursos do projeto, consulte Como migrar recursos do projeto.

Os clientes do Google Workspace e do Cloud Identity podem criar recursos da organização. Cada conta do Google Workspace ou do Cloud Identity está associada a um recurso da organização. Quando existe um recurso da organização, ele é o topo da hierarquia de recursos do Google Cloud, e todos os recursos pertencentes a uma organização são agrupados nele. Isso proporciona visibilidade e controle centralizados sobre todos os recursos que pertencem a um recurso da organização.

Os recursos de pasta são um mecanismo de agrupamento adicional e opcional entre recursos da organização e recursos do projeto. Um recurso da organização é um pré-requisito para usar pastas. Os recursos de pasta e os respectivos recursos do projeto filho são mapeados no recurso da organização.

A hierarquia de recursos do Google Cloud, especialmente na versão mais completa que inclui um recurso de organização e recursos de pasta, permite que as empresas mapeie o recurso da organização no Google Cloud e fornece pontos de anexo lógicos para políticas de gerenciamento de acesso (IAM) e políticas da organização. As políticas do IAM e da organização são herdadas pela hierarquia, e a política efetiva para cada recurso na hierarquia é o resultado das políticas aplicadas diretamente no recurso e das políticas herdadas de seus ancestrais.

O diagrama abaixo representa um exemplo de hierarquia de recursos do Google Cloud no formato completo:
