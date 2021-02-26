* Inicializacao:
  * A automação pega o caminho da pasta a ser processada no arquivo Config dentro da pasta da automação
* Processamento:
  * Inclui em uma array todos os arquivos que estiverem dentro da pasta indicada, menos os arquivos de nome “stats-full-orders-received-...”
  * Extrai dos arquivos
   * O nome dos arquivos contem o dia e horário de envio dos logs. A automação extrai esses valores via regex e insere essa informação na dashboard.  
   * O nome do arquivo também contém o tipo de log: gen, fail e received, respectivamente total, falhos e concluídos. Essa informação é extraída via regex .
* Finalizacao: 
  * Alimenta o arquivo dashboard na pasta da automação e envia e-mail para o destinatário informado no arquivo Config em caso de logs de falhas.
