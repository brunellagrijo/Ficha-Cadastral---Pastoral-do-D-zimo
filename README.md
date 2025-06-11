# Ficha-Cadastral---Pastoral-do-Dizimo
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ficha de Cadastro de Dizimista</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
        }

        .container {
            max-width: 800px;
            margin: 0 auto;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            overflow: hidden;
        }

        .header {
            background: linear-gradient(135deg, #4a5568 0%, #2d3748 100%);
            color: white;
            padding: 30px;
            text-align: center;
            position: relative;
        }

        .header::before {
            content: '✟';
            font-size: 2.5rem;
            position: absolute;
            top: 15px;
            left: 30px;
            opacity: 0.3;
        }

        .header h1 {
            font-size: 2rem;
            margin-bottom: 10px;
            font-weight: 300;
        }

        .header p {
            opacity: 0.9;
            font-size: 1.1rem;
        }

        .form-container {
            padding: 40px;
        }

        .form-section {
            margin-bottom: 35px;
            padding: 25px;
            border: 2px solid #e2e8f0;
            border-radius: 15px;
            background: rgba(247, 250, 252, 0.5);
            transition: all 0.3s ease;
        }

        .form-section:hover {
            border-color: #667eea;
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.1);
        }

        .section-title {
            font-size: 1.3rem;
            color: #2d3748;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid #667eea;
            font-weight: 600;
        }

        .form-row {
            display: flex;
            gap: 20px;
            margin-bottom: 20px;
            flex-wrap: wrap;
        }

        .form-group {
            flex: 1;
            min-width: 200px;
        }

        .form-group.full-width {
            flex: 100%;
        }

        .form-group.half-width {
            flex: 0 0 calc(50% - 10px);
        }

        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
            color: #4a5568;
            font-size: 0.95rem;
        }

        input, select, textarea {
            width: 100%;
            padding: 12px 15px;
            border: 2px solid #e2e8f0;
            border-radius: 10px;
            font-size: 1rem;
            transition: all 0.3s ease;
            background: white;
        }

        input:focus, select:focus, textarea:focus {
            outline: none;
            border-color: #667eea;
            box-shadow: 0 0 0 3px rgba(102, 126, 234, 0.1);
            transform: translateY(-1px);
        }

        textarea {
            resize: vertical;
            min-height: 100px;
        }

        .checkbox-group {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 10px;
        }

        .checkbox-item {
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .checkbox-item input[type="checkbox"] {
            width: auto;
            margin: 0;
        }

        .radio-group {
            display: flex;
            gap: 20px;
            margin-top: 10px;
            flex-wrap: wrap;
        }

        .radio-item {
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .radio-item input[type="radio"] {
            width: auto;
            margin: 0;
        }

        .required {
            color: #e53e3e;
        }

        .button-group {
            display: flex;
            gap: 15px;
            justify-content: center;
            margin-top: 40px;
            padding-top: 30px;
            border-top: 2px solid #e2e8f0;
        }

        button {
            padding: 15px 30px;
            border: none;
            border-radius: 10px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            min-width: 140px;
        }

        .btn-primary {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 25px rgba(102, 126, 234, 0.3);
        }

        .btn-secondary {
            background: #f7fafc;
            color: #4a5568;
            border: 2px solid #e2e8f0;
        }

        .btn-secondary:hover {
            background: #edf2f7;
            border-color: #cbd5e0;
        }

        .info-box {
            background: rgba(102, 126, 234, 0.1);
            border-left: 4px solid #667eea;
            padding: 15px;
            margin-bottom: 20px;
            border-radius: 0 10px 10px 0;
        }

        .info-box p {
            margin: 0;
            color: #4a5568;
            line-height: 1.6;
        }

        @media (max-width: 768px) {
            .form-row {
                flex-direction: column;
            }
            
            .form-group.half-width {
                flex: 100%;
            }
            
            .button-group {
                flex-direction: column;
            }
            
            .header {
                padding: 20px;
            }
            
            .form-container {
                padding: 20px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>Ficha de Cadastro de Dizimista</h1>
            <p>Paróquia/Comunidade Católica</p>
        </div>

        <div class="form-container">
            <div class="info-box">
                <p><strong>Importante:</strong> Todos os dados fornecidos serão tratados com confidencialidade e utilizados exclusivamente para fins pastorais e administrativos da comunidade. Campos marcados com <span class="required">*</span> são obrigatórios.</p>
            </div>

            <form id="cadastroDizimista">
                <!-- Tipo de Cadastro -->
                <div class="form-section">
                    <h3 class="section-title">Tipo de Cadastro</h3>
                    <div class="radio-group">
                        <div class="radio-item">
                            <input type="radio" id="novo" name="tipoCadastro" value="novo" required>
                            <label for="novo">Novo Cadastro</label>
                        </div>
                        <div class="radio-item">
                            <input type="radio" id="atualizacao" name="tipoCadastro" value="atualizacao" required>
                            <label for="atualizacao">Atualização de Dados</label>
                        </div>
                    </div>
                    <div class="form-group" style="margin-top: 15px;">
                        <label for="numeroCarteirinha">Número da Carteirinha (se já possuir):</label>
                        <input type="text" id="numeroCarteirinha" name="numeroCarteirinha">
                    </div>
                </div>

                <!-- Dados Pessoais -->
                <div class="form-section">
                    <h3 class="section-title">Dados Pessoais</h3>
                    
                    <div class="form-row">
                        <div class="form-group">
                            <label for="nomeCompleto">Nome Completo <span class="required">*</span></label>
                            <input type="text" id="nomeCompleto" name="nomeCompleto" required>
                        </div>
                    </div>

                    <div class="form-row">
                        <div class="form-group half-width">
                            <label for="cpf">CPF <span class="required">*</span></label>
                            <input type="text" id="cpf" name="cpf" required>
                        </div>
                        <div class="form-group half-width">
                            <label for="rg">RG</label>
                            <input type="text" id="rg" name="rg">
                        </div>
                    </div>

                    <div class="form-row">
                        <div class="form-group half-width">
                            <label for="dataNascimento">Data de Nascimento <span class="required">*</span></label>
                            <input type="date" id="dataNascimento" name="dataNascimento" required>
                        </div>
                        <div class="form-group half-width">
                            <label for="estadoCivil">Estado Civil</label>
                            <select id="estadoCivil" name="estadoCivil">
                                <option value="">Selecione...</option>
                                <option value="solteiro">Solteiro(a)</option>
                                <option value="casado">Casado(a)</option>
                                <option value="divorciado">Divorciado(a)</option>
                                <option value="viuvo">Viúvo(a)</option>
                                <option value="uniao_estavel">União Estável</option>
                            </select>
                        </div>
                    </div>

                    <div class="form-row">
                        <div class="form-group half-width">
                            <label for="profissao">Profissão</label>
                            <input type="text" id="profissao" name="profissao">
                        </div>
                        <div class="form-group half-width">
                            <label for="escolaridade">Escolaridade</label>
                            <select id="escolaridade" name="escolaridade">
                                <option value="">Selecione...</option>
                                <option value="fundamental_incompleto">Ensino Fundamental Incompleto</option>
                                <option value="fundamental_completo">Ensino Fundamental Completo</option>
                                <option value="medio_incompleto">Ensino Médio Incompleto</option>
                                <option value="medio_completo">Ensino Médio Completo</option>
                                <option value="superior_incompleto">Ensino Superior Incompleto</option>
                                <option value="superior_completo">Ensino Superior Completo</option>
                                <option value="pos_graduacao">Pós-graduação</option>
                            </select>
                        </div>
                    </div>
                </div>

                <!-- Contato -->
                <div class="form-section">
                    <h3 class="section-title">Dados de Contato</h3>
                    
                    <div class="form-row">
                        <div class="form-group half-width">
                            <label for="telefone">Telefone Fixo</label>
                            <input type="tel" id="telefone" name="telefone">
                        </div>
                        <div class="form-group half-width">
                            <label for="celular">Celular <span class="required">*</span></label>
                            <input type="tel" id="celular" name="celular" required>
                        </div>
                    </div>

                    <div class="form-row">
                        <div class="form-group">
                            <label for="email">E-mail</label>
                            <input type="email" id="email" name="email">
                        </div>
                    </div>
                </div>

                <!-- Endereço -->
                <div class="form-section">
                    <h3 class="section-title">Endereço</h3>
                    
                    <div class="form-row">
                        <div class="form-group">
                            <label for="endereco">Logradouro (Rua, Avenida, etc.) <span class="required">*</span></label>
                            <input type="text" id="endereco" name="endereco" required>
                        </div>
                    </div>

                    <div class="form-row">
                        <div class="form-group half-width">
                            <label for="numero">Número <span class="required">*</span></label>
                            <input type="text" id="numero" name="numero" required>
                        </div>
                        <div class="form-group half-width">
                            <label for="complemento">Complemento</label>
                            <input type="text" id="complemento" name="complemento">
                        </div>
                    </div>

                    <div class="form-row">
                        <div class="form-group half-width">
                            <label for="bairro">Bairro <span class="required">*</span></label>
                            <input type="text" id="bairro" name="bairro" required>
                        </div>
                        <div class="form-group half-width">
                            <label for="cep">CEP <span class="required">*</span></label>
                            <input type="text" id="cep" name="cep" required>
                        </div>
                    </div>

                    <div class="form-row">
                        <div class="form-group half-width">
                            <label for="cidade">Cidade <span class="required">*</span></label>
                            <input type="text" id="cidade" name="cidade" required>
                        </div>
                        <div class="form-group half-width">
                            <label for="estado">Estado <span class="required">*</span></label>
                            <select id="estado" name="estado" required>
                                <option value="">Selecione...</option>
                                <option value="AC">Acre</option>
                                <option value="AL">Alagoas</option>
                                <option value="AP">Amapá</option>
                                <option value="AM">Amazonas</option>
                                <option value="BA">Bahia</option>
                                <option value="CE">Ceará</option>
                                <option value="DF">Distrito Federal</option>
                                <option value="ES">Espírito Santo</option>
                                <option value="GO">Goiás</option>
                                <option value="MA">Maranhão</option>
                                <option value="MT">Mato Grosso</option>
                                <option value="MS">Mato Grosso do Sul</option>
                                <option value="MG">Minas Gerais</option>
                                <option value="PA">Pará</option>
                                <option value="PB">Paraíba</option>
                                <option value="PR">Paraná</option>
                                <option value="PE">Pernambuco</option>
                                <option value="PI">Piauí</option>
                                <option value="RJ">Rio de Janeiro</option>
                                <option value="RN">Rio Grande do Norte</option>
                                <option value="RS">Rio Grande do Sul</option>
                                <option value="RO">Rondônia</option>
                                <option value="RR">Roraima</option>
                                <option value="SC">Santa Catarina</option>
                                <option value="SP">São Paulo</option>
                                <option value="SE">Sergipe</option>
                                <option value="TO">Tocantins</option>
                            </select>
                        </div>
                    </div>
                </div>

                <!-- Dados Familiares -->
                <div class="form-section">
                    <h3 class="section-title">Dados Familiares</h3>
                    
                    <div class="form-row">
                        <div class="form-group half-width">
                            <label for="conjugeNome">Nome do Cônjuge</label>
                            <input type="text" id="conjugeNome" name="conjugeNome">
                        </div>
                        <div class="form-group half-width">
                            <label for="conjugeDataNascimento">Data de Nascimento do Cônjuge</label>
                            <input type="date" id="conjugeDataNascimento" name="conjugeDataNascimento">
                        </div>
                    </div>

                    <div class="form-row">
                        <div class="form-group half-width">
                            <label for="numeroFilhos">Número de Filhos</label>
                            <input type="number" id="numeroFilhos" name="numeroFilhos" min="0">
                        </div>
                        <div class="form-group half-width">
                            <label for="filhosMenores">Filhos Menores de 18 anos</label>
                            <input type="number" id="filhosMenores" name="filhosMenores" min="0">
                        </div>
                    </div>

                    <div class="form-row">
                        <div class="form-group full-width">
                            <label for="observacoesFamilia">Observações sobre a Família (opcional)</label>
                            <textarea id="observacoesFamilia" name="observacoesFamilia" placeholder="Informações adicionais sobre a composição familiar, filhos com necessidades especiais, etc."></textarea>
                        </div>
                    </div>
                </div>

                <!-- Dados Pastorais -->
                <div class="form-section">
                    <h3 class="section-title">Dados Pastorais</h3>
                    
                    <div class="form-row">
                        <div class="form-group half-width">
                            <label for="dataBatismo">Data do Batismo</label>
                            <input type="date" id="dataBatismo" name="dataBatismo">
                        </div>
                        <div class="form-group half-width">
                            <label for="localBatismo">Local do Batismo</label>
                            <input type="text" id="localBatismo" name="localBatismo">
                        </div>
                    </div>

                    <div class="form-row">
                        <div class="form-group half-width">
                            <label for="dataCrisma">Data da Crisma</label>
                            <input type="date" id="dataCrisma" name="dataCrisma">
                        </div>
                        <div class="form-group half-width">
                            <label for="localCrisma">Local da Crisma</label>
                            <input type="text" id="localCrisma" name="localCrisma">
                        </div>
                    </div>

                    <div class="form-row">
                        <div class="form-group">
                            <label>Sacramentos Recebidos:</label>
                            <div class
