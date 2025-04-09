<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Inscrição Guia Policiamento Extraordinário</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
        }
    </style>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        'inter': ['Inter', 'sans-serif'],
                    },
                },
            },
        }
    </script>
</head>
<body class="bg-gray-100 flex justify-center items-center min-h-screen p-4">
    <div class="bg-white rounded-lg shadow-md w-full max-w-2xl p-6">
        <h1 class="text-2xl font-semibold text-blue-600 mb-4 text-center">Inscrição para Guia de Policiamento Extraordinário - 2ªCia/BPTur</h1>
        <form id="inscricao-form" class="space-y-4">
            <div id="passo1" class="bloco-passo">
                <h2 class="text-xl font-semibold text-gray-800 mb-2">Passo 1: Dados Pessoais</h2>
                <div class="mb-4">
                    <label for="nome" class="block text-gray-700 text-sm font-bold mb-2">Nome Completo:</label>
                    <input type="text" id="nome" name="nome" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" required>
                    <div id="nome-erro" class="text-red-500 text-xs italic" style="display: none;"></div>
                </div>
                <div class="mb-4">
                    <label for="numeral" class="block text-gray-700 text-sm font-bold mb-2">Numeral:</label>
                    <input type="text" id="numeral" name="numeral" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline">
                    <div id="numeral-erro" class="text-red-500 text-xs italic" style="display: none;"></div>
                </div>
                <div class="mb-4">
                    <label for="posto" class="block text-gray-700 text-sm font-bold mb-2">Posto/Graduação:</label>
                    <select id="posto" name="posto" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" required>
                        <option value="">Selecione...</option>
                        <option value="Soldado">Soldado</option>
                        <option value="Cabo">Cabo</option>
                        <option value="3º Sargento">3º Sargento</option>
                        <option value="2º Sargento">2º Sargento</option>
                        <option value="1º Sargento">1º Sargento</option>
                        <option value="Subtenente">Subtenente</option>
                        <option value="2º Tenente">2º Tenente</option>
                        <option value="1º Tenente">1º Tenente</option>
                        <option value="Capitão">Capitão</option>
                    </select>
                    <div id="posto-erro" class="text-red-500 text-xs italic" style="display: none;"></div>
                </div>
                <div class="mb-4">
                    <label for="nome-guerra" class="block text-gray-700 text-sm font-bold mb-2">Nome de Guerra:</label>
                    <input type="text" id="nome-guerra" name="nome-guerra" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" required>
                    <div id="nome-guerra-erro" class="text-red-500 text-xs italic" style="display: none;"></div>
                </div>
                <div class="mb-4">
                    <label for="unidade" class="block text-gray-700 text-sm font-bold mb-2">Unidade:</label>
                    <select id="unidade" name="unidade" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" required>
                        <option value="">Selecione...</option>
                        <option value="Bptur">Bptur</option>
                        <option value="Outras">Outras</option>
                    </select>
                    <div id="unidade-erro" class="text-red-500 text-xs italic" style="display: none;"></div>
                </div>
            </div>

            <div id="passo2" class="bloco-passo" style="display: none;">
                <h2 class="text-xl font-semibold text-gray-800 mb-2">Passo 2: Contato e Serviço</h2>
                <div class="mb-4">
                    <label for="telefone" class="block text-gray-700 text-sm font-bold mb-2">Telefone para Contato:</label>
                    <input type="text" id="telefone" name="telefone" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" required>
                    <div id="telefone-erro" class="text-red-500 text-xs italic" style="display: none;"></div>
                </div>
                <div class="mb-4">
                    <label for="servico-ordinario" class="block text-gray-700 text-sm font-bold mb-2">Você estará escalado no serviço ordinário no dia que se voluntariar para a DRSO?</label>
                    <select id="servico-ordinario" name="servico-ordinario" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" required>
                        <option value="">Selecione...</option>
                        <option value="Sim">Sim</option>
                        <option value="Não">Não</option>
                    </select>
                    <div id="servico-ordinario-erro" class="text-red-500 text-xs italic" style="display: none;"></div>
                    <div id="servico-ordinario-alerta" class="mt-2 text-yellow-600 font-semibold" style="display: none;">Você não pode se voluntariar para a DRSO se estiver escalado no serviço ordinário.</div>
                </div>
            </div>

            <div id="passo3" class="bloco-passo" style="display: none;">
                <h2 class="text-xl font-semibold text-gray-800 mb-2">Passo 3: Disponibilidade e Local/Função</h2>
                <div class="mb-4">
                    <label for="disponibilidade" class="block text-gray-700 text-sm font-bold mb-2">Disponibilidade de Dias:</label>
                    <div id="disponibilidade-erro" class="text-red-500 text-xs italic mb-2" style="display: none;"></div>
                    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-4">
                        <div>
                            <label for="quinta" class="inline-flex items-center">
                                <input type="checkbox" id="quinta" name="disponibilidade[]" value="quinta" class="form-checkbox h-5 w-5 text-blue-600 rounded">
                                <span class="ml-2 text-gray-700 text-sm">Quinta (09/05/2024)</span>
                            </label>
                        </div>
                        <div>
                            <label for="sexta" class="inline-flex items-center">
                                <input type="checkbox" id="sexta" name="disponibilidade[]" value="sexta" class="form-checkbox h-5 w-5 text-blue-600 rounded">
                                <span class="ml-2 text-gray-700 text-sm">Sexta (10/05/2024)</span>
                            </label>
                        </div>
                        <div>
                            <label for="sabado" class="inline-flex items-center">
                                <input type="checkbox" id="sabado" name="disponibilidade[]" value="sabado" class="form-checkbox h-5 w-5 text-blue-600 rounded">
                                <span class="ml-2 text-gray-700 text-sm">Sábado (11/05/2024)</span>
                            </label>
                        </div>
                        <div>
                            <label for="domingo" class="inline-flex items-center">
                                <input type="checkbox" id="domingo" name="disponibilidade[]" value="domingo" class="form-checkbox h-5 w-5 text-blue-600 rounded">
                                <span class="ml-2 text-gray-700 text-sm">Domingo (12/05/2024)</span>
                            </label>
                        </div>
                    </div>
                </div>
                <div class="mb-4">
                    <label for="local-funcao" class="block text-gray-700 text-sm font-bold mb-2">Local de Emprego/Função:</label>
                    <div id="local-funcao-opcoes" class="grid grid-cols-1 sm:grid-cols-2 gap-2">
                        <label for="Aranau" class="inline-flex items-center">
                            <input type="checkbox" id="Aranau" name="local-funcao[]" value="Aranau" class="form-checkbox h-5 w-5 text-blue-600 rounded">
                            <span class="ml-2 text-gray-700 text-sm">Aranaú</span>
                        </label>
                        <label for="Prea" class="inline-flex items-center">
                            <input type="checkbox" id="Prea" name="local-funcao[]" value="Prea" class="form-checkbox h-5 w-5 text-blue-600 rounded">
                            <span class="ml-2 text-gray-700 text-sm">Preá</span>
                        </label>
                        <label for="Jericoacoara" class="inline-flex items-center">
                            <input type="checkbox" id="Jericoacoara" name="local-funcao[]" value="Jericoacoara" class="form-checkbox h-5 w-5 text-blue-600 rounded">
                            <span class="ml-2 text-gray-700 text-sm">Jericoacoara</span>
                        </label>
                         <label for="Outros" class="inline-flex items-center">
                            <input type="checkbox" id="Outros" name="local-funcao[]" value="Outros" class="form-checkbox h-5 w-5 text-blue-600 rounded">
                            <span class="ml-2 text-gray-700 text-sm">Outros</span>
                        </label>
                    </div>
                    <div id="local-funcao-erro" class="text-red-500 text-xs italic" style="display: none;"></div>
                </div>
            </div>

            <div id="passo4" class="bloco-passo" style="display: none;">
                <h2 class="text-xl font-semibold text-gray-800 mb-2">Passo 4: Observações e Conclusão</h2>
                <div class="mb-4">
                    <label for="observacoes" class="block text-gray-700 text-sm font-bold mb-2">Observações:</label>
                    <textarea id="observacoes" name="observacoes" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline h-32 resize-y"></textarea>
                    <div id="observacoes-erro" class="text-red-500 text-xs italic" style="display: none;"></div>
                </div>
                
            </div>

            <div class="flex justify-between mt-4">
                <button type="button" id="anterior" class="bg-gray-300 hover:bg-gray-400 text-gray-800 font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline" style="display: none;">Anterior</button>
                <button type="submit" id="proximo" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline">Próximo Passo</button>
            </div>
        </form>
        <div id="mensagem-erro-geral" class="mt-4 text-red-500 font-semibold border border-red-500 rounded p-4" style="display: none;"></div>
    </div>

    <script>
        const form = document.getElementById('inscricao-form');
        const passos = document.querySelectorAll('.bloco-passo');
        const anteriorButton = document.getElementById('anterior');
        const proximoButton = document.getElementById('proximo');
        const mensagemErroGeral = document.getElementById('mensagem-erro-geral');
        let passoAtual = 0;

        function mostrarPasso(passo) {
            passos.forEach((p, index) => {
                p.style.display = index === passo ? 'block' : 'none';
            });
            anteriorButton.style.display = passo > 0 ? 'inline-block' : 'none';
            proximoButton.textContent = passo === passos.length - 1 ? 'Enviar Inscrição' : 'Próximo Passo';
            mensagemErroGeral.style.display = 'none';
            passoAtual = passo;
        }

        function validarPasso(passo) {
            let valido = true;
            mensagemErroGeral.style.display = 'none';

            if (passo === 0) {
                valido = validarCampo('nome', 'Nome Completo é obrigatório') && valido;
                valido = validarCampo('nome-guerra', 'Nome de Guerra é obrigatório') && valido;
                valido = validarCampo('posto', 'Posto/Graduação é obrigatório') && valido;
                valido = validarCampo('unidade', 'Unidade é obrigatória') && valido;
            } else if (passo === 1) {
                valido = validarCampo('telefone', 'Telefone para Contato é obrigatório') && valido;
                // Removendo a validação de formato do telefone
                //valido = validarTelefone('telefone') && valido;
                valido = validarCampo('servico-ordinario', 'Você estará escalado no serviço ordinário é obrigatório') && valido;
                if (document.getElementById('servico-ordinario').value === 'Sim') {
                    mensagemErroGeral.textContent = "Você não pode se voluntariar para a DRSO se estiver escalado no serviço ordinário.";
                    mensagemErroGeral.style.display = 'block';
                    return false;
                }
            } else if (passo === 2) {
                valido = validarDisponibilidade() && valido;
                valido = validarLocalFuncao() && valido; // Adicionando validação para Local de Emprego/Função
            }
            return valido;
        }

        function validarCampo(campoId, mensagemErro) {
            const campo = document.getElementById(campoId);
            const erro = document.getElementById(campoId + '-erro');
            if (!campo.value.trim()) {
                erro.textContent = mensagemErro;
                erro.style.display = 'block';
                campo.classList.add('border-red-500');
                return false;
            } else {
                erro.style.display = 'none';
                campo.classList.remove('border-red-500');
                return true;
            }
        }

        function validarTelefone(campoId) {
            const campo = document.getElementById(campoId);
            const erro = document.getElementById(campoId + '-erro');
            const regexTelefone = /^\(\d{2}\) \d{4,5}-\d{4}$/;
            if (!regexTelefone.test(campo.value.trim())) {
                erro.textContent = 'Formato de telefone inválido. Use (XX) XXXX-XXXX ou (XX) XXXXX-XXXX.';
                erro.style.display = 'block';
                campo.classList.add('border-red-500');
                return false;
            } else {
                erro.style.display = 'none';
                campo.classList.remove('border-red-500');
                return true;
            }
        }

        function validarDisponibilidade() {
            const checkboxes = document.querySelectorAll('input[name="disponibilidade[]"]:checked');
            const erro = document.getElementById('disponibilidade-erro');
            if (checkboxes.length === 0) {
                erro.textContent = 'Selecione pelo menos um dia de disponibilidade.';
                erro.style.display = 'block';
                return false;
            } else {
                erro.style.display = 'none';
                return true;
            }
        }

        function validarLocalFuncao() {
            const checkboxes = document.querySelectorAll('input[name="local-funcao[]"]:checked');
            const erro = document.getElementById('local-funcao-erro');
            if (checkboxes.length === 0) {
                erro.textContent = 'Selecione pelo menos um Local de Emprego/Função.';
                erro.style.display = 'block';
                return false;
            } else {
                erro.style.display = 'none';
                return true;
            }
        }

        function avancarPasso() {
            if (validarPasso(passoAtual)) {
                if (passoAtual < passos.length - 1) {
                    mostrarPasso(passoAtual + 1);
                } else {
                    // Se estiver no último passo, submete o formulário
                    form.dispatchEvent(new Event('submit'));
                }
            }
        }

        function retrocederPasso() {
            if (passoAtual > 0) {
                mostrarPasso(passoAtual - 1);
            }
        }

        form.addEventListener('submit', (event) => {
            event.preventDefault();
            if (validarPasso(passoAtual)) {
                // Aqui você pode enviar os dados do formulário para o servidor
                // usando fetch ou outra técnica de requisição.
                // Exemplo de como pegar os dados do formulário:
                const formData = new FormData(form);
                const dados = {};
                 formData.forEach((valor, chave) => {
                    if (chave === 'disponibilidade[]' || chave === 'local-funcao[]') {
                        if (!dados[chave]) {
                            dados[chave] = [];
                        }
                        dados[chave].push(valor);
                    } else {
                        dados[chave] = valor;
                    }
                });
                console.log(dados); // Exibe os dados no console para verificação

                // Exemplo de envio dos dados usando fetch (adapte a URL):
                /*
                fetch('/sua-api-para-inscricao', {
                    method: 'POST',
                    headers: {
                        'Content-Type': 'application/json',
                    },
                    body: JSON.stringify(dados),
                })
                .then(response => {
                    if (response.ok) {
                        alert('Inscrição realizada com sucesso!');
                        form.reset(); // Limpa o formulário
                        mostrarPasso(0); // Volta para o primeiro passo
                    } else {
                        alert('Erro ao realizar inscrição. Tente novamente.');
                    }
                })
                .catch(error => {
                    console.error('Erro:', error);
                    alert('Erro ao realizar inscrição. Tente novamente.');
                });
                */
            }
        });

        anteriorButton.addEventListener('click', retrocederPasso);
        proximoButton.addEventListener('click', avancarPasso);

        mostrarPasso(0); // Inicializa o formulário no primeiro passo
    </script>
</body>
</html>
