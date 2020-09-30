		<div class="page-header">
			<h2>Adicionais<br><small>Aberto a toda comunidade de desenvolvedores</small></h2>
		</div>

		<div class="tabbable" style="margin-top:10px">
			<!-- Only required for left/right tabs -->
			<ul class="nav nav-pills">
				<li class="active"><a href="#tab1" data-toggle="tab">Marcadores
						rápidos</a></li>
				<li><a href="#tab2" data-toggle="tab">Estatísticas</a></li>
				<li><a href="#tab3" data-toggle="tab">Gerador de código</a></li>
			</ul>
			<div class="tab-content">
				<div class="tab-pane active" id="tab1">
					<p class="lead">Criar marcos nos arquivos-fontes para acesso rápido.</p>
					<ol>
						<li>Abra o arquivo para edição, posicione na linha desejada e
							acione <code>Alt + M</code>, na sequência acione um número entre 0 e
							9, que será associado ao marco.
						</li>
						<li>Para ir ao marco acione <code>Alt + M</code>, na sequência o
							número dele.
						</li>
						<li>Para remover, primeiro vá ao marco que deseja remover e acione
							<code>Alt + M</code> e na sequência o número do marco.
						</li>
						<li>Para adicionar um marco na próxima posição livre, acione <code>Alt
			+ M</code>, seguido de <code>NUMPAD_ADD</code>.
						</li>
						<li>Para remover todos os marcos, acione <code>Alt + M</code>,
							seguido de <code>NUMPAD_SUBTRACT</code>.
						</li>
						<li>Para navegar entre as anotações (e marcos), acione <code>Ctrl
			+ .</code> para a próxima e <code>Ctrl + ,</code> para a anterior.
						</li>
					</ol>
					<p>
						Para instruções detalhadas, acesse <a href="https://sourceforge.net/p/actools/wiki/Marcos"
							target="_blank">
							Wiki: Marcos<span class="glyphicon glyphicon-link" aria-hidden="false"></span></a>
					</p>

				</div>
				<div class="tab-pane" id="tab2">
					<p class="lead">Apresenta uma série de estatísticas curiosas sobre
						seus programas fontes.</p>
					<h4>Como usar</h4>
					<ol>
						<li>Selecione o recurso-alvo. Se for um projeto ou pasta, os
							filhos serão processados.</li>
						<li>Acione o menu de contexto, opção "<code>AC Ferramentas
			| Estatisticas</code>".<br> <img src="./images/statistic/statistics_001.png"></li>
						<li>Aguarde o processamento. Ao final, lhe será apresentado o
							resultado.<br> <img src="./images/statistic/statistics_002.png">
						</li>
						<li>Pode configurar quais processos serão executados, acesse <code>Janelas
			| Preferências</code>, <code>AC Ferramentas + Estatísticas</code>.<br>
							<img src="./images/statistic/statistics_003.png">
						</li>
					</ol>
					<h4>Base estatística</h4>
					<p>
						Você pode colaborar enviando suas estatísticas para a nossa base
						preenchendo algumas informações. Acesse
						<code>Janelas | Preferências</code>
						,
						<code>AC Ferramentas + Estatísticas + Envio de Dados</code>
						.<br> Os dados enviados que podem identificá-lo são criptografados
						antes, não sendo possível recuperar a informação original.<br> <img
							src="./images/statistic/statistics_004.png">
					</p>
					<p>
						Para instruções detalhadas, acesse <a href="https://sourceforge.net/p/actools/wiki/Estatisticas"
							target="_blank">
							Wiki: Estatísticas<span class="glyphicon glyphicon-link" aria-hidden="false"></span></a>
					</p>



				</div>
				<div class="tab-pane" id="tab3">
					<p class="lead">Gera código AdvPL a partir de diagramas UML.</p>
					<p class="alert alert-danger">
						<b>Experimental</b>: Poderá ocorrer mudanças em procedimentos ou mesmo
						no resultado final esperado. Recursos poderão ser adicionados ou
						removidos sem prévio aviso. NÃO USE EM PRODUÇÃO.
					</p>

					<p class="alert alert-info">
						<b>Importante</b>: Apenas os diagramas e elementos abaixo citados são
						suportados.<br>Muitos elementos são emulações devido a
						características da linguagem alvo.
					</p>

					<div class="panel panel-info">
						<div class="panel-heading">
							<h4 class="panel-title">Diagrama de Classes</h4>
						</div>
						<table class="table">
							<tr>
								<td>Class</td>
								<td>Não suporta definições internas.<br> Definições de
									visibilidade são utilizadas somente na documentação ProtheusDOC.
								</td>
							</tr>
							<tr>
								<td>Enumeration</td>
								<td>Emulado através de uma classe.<br>
								</td>
							</tr>
							<tr>
								<td>Interface</td>
								<td>Emulado através de um arquivo de definição, que é incluído
									na definição da classe que deve implementar a interface.<br>
							</tr>
						</table>
					</div>

					<h4>Preparação</h4>
					<ol>
						<li>Instale o adicional para UML Papyrus, via sítio de atualização
							do Luna.<br> Acesse <a href="http://eclipse.org/papyrus/" target="_blank">sítio do
								projeto<span class="glyphicon glyphicon-link" aria-hidden="false"></span></a> para
							saber mais.
						</li>

						<li>Adicione o sítio de atualização de adicionais extras do
							Papyrus. Não é preciso instalar nenhum adicional.<br>
							<img src="./images/codegen/codegen006.png">
							<p class="alert alert-info">
								<b>Sítio com extras do Papyrus</b>:
								<code>http://download.eclipse.org/modeling/mdt/papyrus/updates/releases/luna/extra</code>
							</p>
						</li>

						<li>Instale "AC Ferramentas: Gerador de Código" a partir do nosso
							sítio de atualização (<a href="install.html" target="_blank">detalhes<span
									class="glyphicon glyphicon-link" aria-hidden="false"></span></a>).
						</li>
						<li>Encerre o TDS e adicione (ou alterere) as linhas abaixo no
							arquivo de configuração <code>TDS_HOME/developerStudio.ini</code>.<br>
							<br>
							<pre>
  -Xms512m
  -Xmx1024m
  -XX:+UseParallelGC
  -XX:PermSize=256M
  -XX:MaxPermSize=512M</pre>
						</li>
					</ol>

					<h4>Como usar</h4>
					<ol>
						<li>Abra o arquivo de modelagem (<code>DI</code>), que contem o
							diagrama de classes.<br> <img src="./images/codegen/codegen001.png"></li>
						<li>Acione o "<code>Geração de código AdvPL</code>" na barra de
							ferramentas.<br> <img src="./images/codegen/codegen002.png"></li>
						<li>Selecione o projeto onde serão salvo os arquivos.<br> <img
								src="./images/codegen/codegen003.png"></li>
						<li>Aguarde o processamento e ao final terá o código gerado.
							<p class="alert alert-danger">
								<b>Cuidado</b>: Ao gerar o código, os arquivos-fontes anteriores
								serão eliminados. Faça cópias de segurança antes e depois compare os
								fontes gerados e ajuste conforme necessário.<br> <br>
								Estamos trabalhando para que o processo de geração de fontes mantenha
								o código escrito por você.
							</p> <img src="./images/codegen/codegen004.png">
						</li>

						<li>Para configurar o nomeamento de arquivo e outras
							características, acesse <code>Janelas | Preferências</code>, <code>AC
			Ferramentas + Geração de código AdvPL</code>.<br> <img src="./images/codegen/codegen005.png">
						</li>
					</ol>
					<p>
						Para instruções detalhadas, acesse <a href="https://sourceforge.net/p/actools/wiki/Codegen"
							target="_blank">
							Wiki: Geração de código<span class="glyphicon glyphicon-link" aria-hidden="false"></span>
						</a>
					</p>


				</div>
			</div>
		</div>
