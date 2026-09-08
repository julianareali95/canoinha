# canoinha
gestão de canoas
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>canoa teste</title>

<style>
:root {
    --verde: #087f8c;
    --verde-escuro: #075963;
    --azul: #2563eb;
    --verde-claro: #e7f7f8;
    --fundo: #f4f8f9;
    --branco: #ffffff;
    --texto: #173042;
    --cinza: #6b7c85;
    --borda: #e2eaed;
    --sucesso: #16a34a;
    --alerta: #d97706;
    --erro: #dc2626;
    --sombra: 0 5px 20px rgba(0,0,0,.06);
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, Helvetica, sans-serif;
    background: var(--fundo);
    color: var(--texto);
}

/* SIDEBAR */

.sidebar {
    position: fixed;
    left: 0;
    top: 0;
    bottom: 0;
    width: 250px;
    background: var(--verde-escuro);
    color: white;
    padding: 25px 14px;
    z-index: 1000;
}

.logo {
    font-size: 23px;
    font-weight: bold;
    padding: 5px 15px 30px;
}

.logo span {
    color: #57d9dc;
}

.menu-title {
    color: #8eb6ba;
    font-size: 11px;
    text-transform: uppercase;
    letter-spacing: 1px;
    padding: 15px;
}

.menu button {
    display: block;
    width: 100%;
    border: 0;
    background: transparent;
    color: #d9edef;
    padding: 13px 15px;
    margin: 3px 0;
    border-radius: 9px;
    text-align: left;
    cursor: pointer;
    font-size: 14px;
}

.menu button:hover,
.menu button.active {
    background: #0b6974;
    color: white;
}

.menu button .icon {
    width: 25px;
    display: inline-block;
}

/* MAIN */

.main {
    margin-left: 250px;
    min-height: 100vh;
}

.topbar {
    height: 72px;
    background: white;
    border-bottom: 1px solid var(--borda);
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 30px;
}

.topbar-title {
    font-size: 21px;
    font-weight: bold;
}

.user {
    display: flex;
    align-items: center;
    gap: 10px;
}

.avatar {
    width: 40px;
    height: 40px;
    background: var(--verde);
    color: white;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: bold;
}

.mobile-menu {
    display: none;
    border: 0;
    background: transparent;
    font-size: 25px;
    cursor: pointer;
}

.content {
    padding: 30px;
}

/* SEÇÕES */

.section {
    display: none;
}

.section.active {
    display: block;
}

.section-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
}

.section-header h2 {
    font-size: 21px;
}

.section-header p {
    color: var(--cinza);
    font-size: 13px;
    margin-top: 5px;
}

/* BOTÕES */

.btn {
    border: 0;
    padding: 11px 16px;
    border-radius: 8px;
    cursor: pointer;
    font-weight: bold;
    font-size: 13px;
}

.btn-primary {
    background: var(--verde);
    color: white;
}

.btn-primary:hover {
    background: var(--verde-escuro);
}

.btn-secondary {
    background: var(--verde-claro);
    color: var(--verde-escuro);
}

.btn-danger {
    background: #fee2e2;
    color: var(--erro);
}

/* CARDS */

.cards {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 18px;
    margin-bottom: 25px;
}

.card {
    background: var(--branco);
    border: 1px solid var(--borda);
    border-radius: 14px;
    padding: 20px;
    box-shadow: var(--sombra);
}

.stat {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.stat p {
    color: var(--cinza);
    font-size: 13px;
}

.stat h3 {
    font-size: 29px;
    margin-top: 7px;
}

.stat-icon {
    width: 48px;
    height: 48px;
    border-radius: 12px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 22px;
}

.green {
    background: #dcfce7;
}

.blue {
    background: #dbeafe;
}

.yellow {
    background: #fef3c7;
}

.red {
    background: #fee2e2;
}

/* GRID */

.dashboard-grid {
    display: grid;
    grid-template-columns: 1.5fr 1fr;
    gap: 20px;
}

/* TABELA */

.table-container {
    background: white;
    border: 1px solid var(--borda);
    border-radius: 14px;
    overflow: auto;
    box-shadow: var(--sombra);
}

table {
    width: 100%;
    border-collapse: collapse;
    min-width: 700px;
}

th,
td {
    padding: 14px 17px;
    border-bottom: 1px solid var(--borda);
    text-align: left;
    font-size: 13px;
}

th {
    background: #f8fbfc;
    color: var(--cinza);
    font-size: 12px;
}

tr:last-child td {
    border-bottom: 0;
}

/* STATUS */

.badge {
    display: inline-block;
    border-radius: 30px;
    padding: 6px 10px;
    font-size: 11px;
    font-weight: bold;
}

.disponivel {
    background: #dcfce7;
    color: #15803d;
}

.em-uso {
    background: #dbeafe;
    color: #1d4ed8;
}

.reservada {
    background: #fef3c7;
    color: #a16207;
}

.manutencao {
    background: #fee2e2;
    color: #b91c1c;
}

/* BUSCA */

.search-box {
    background: white;
    border: 1px solid var(--borda);
    border-radius: 10px;
    padding: 15px;
    margin-bottom: 18px;
}

.search {
    width: 280px;
    max-width: 100%;
    border: 1px solid var(--borda);
    border-radius: 8px;
    padding: 11px;
    outline: none;
}

.search:focus {
    border-color: var(--verde);
}

/* ATIVIDADES */

.activity {
    list-style: none;
}

.activity li {
    display: flex;
    gap: 12px;
    padding: 14px 0;
    border-bottom: 1px solid var(--borda);
}

.activity li:last-child {
    border-bottom: 0;
}

.activity-icon {
    width: 38px;
    height: 38px;
    border-radius: 9px;
    background: var(--verde-claro);
    display: flex;
    align-items: center;
    justify-content: center;
}

.activity small {
    display: block;
    color: var(--cinza);
    margin-top: 4px;
}

/* MAPA */

.map {
    height: 400px;
    position: relative;
    overflow: hidden;
    border-radius: 14px;
    background:
        linear-gradient(135deg,#dff3f5,#edf8f9);
}

.water {
    position: absolute;
    width: 75%;
    height: 150%;
    left: 15%;
    top: -25%;
    background: #bde8ee;
    transform: rotate(22deg);
    border-radius: 50%;
}

.marker {
    position: absolute;
    z-index: 3;
    background: var(--verde);
    color: white;
    padding: 9px 12px;
    border-radius: 20px;
    font-size: 11px;
    font-weight: bold;
    box-shadow: 0 5px 15px rgba(0,0,0,.15);
}

.m1 { left: 20%; top: 25%; }
.m2 { left: 55%; top: 45%; }
.m3 { left: 72%; top: 22%; }
.m4 { left: 40%; top: 72%; }

/* MODAL */

.modal {
    position: fixed;
    inset: 0;
    background: rgba(0,0,0,.45);
    display: none;
    align-items: center;
    justify-content: center;
    padding: 20px;
    z-index: 3000;
}

.modal.show {
    display: flex;
}

.modal-box {
    background: white;
    width: 100%;
    max-width: 650px;
    max-height: 90vh;
    overflow-y: auto;
    border-radius: 16px;
    padding: 25px;
}

.modal-header {
    display: flex;
    justify-content: space-between;
    margin-bottom: 22px;
}

.modal-header h2 {
    font-size: 20px;
}

.close {
    background: transparent;
    border: 0;
    font-size: 27px;
    cursor: pointer;
    color: var(--cinza);
}

.form-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 15px;
}

.form-group {
    display: flex;
    flex-direction: column;
    gap: 6px;
}

.full {
    grid-column: 1 / -1;
}

label {
    color: #526773;
    font-size: 12px;
    font-weight: bold;
}

input,
select,
textarea {
    width: 100%;
    border: 1px solid var(--borda);
    padding: 11px;
    border-radius: 8px;
    outline: none;
    font-family: inherit;
}

textarea {
    min-height: 90px;
    resize: vertical;
}

input:focus,
select:focus,
textarea:focus {
    border-color: var(--verde);
}

.modal-footer {
    display: flex;
    justify-content: flex-end;
    gap: 10px;
    margin-top: 22px;
}

/* RESPONSIVO */

@media(max-width: 1050px) {

    .cards {
        grid-template-columns: repeat(2,1fr);
    }

    .dashboard-grid {
        grid-template-columns: 1fr;
    }

}

@media(max-width: 700px) {

    .sidebar {
        transform: translateX(-100%);
        transition: .25s;
    }

    .sidebar.open {
        transform: translateX(0);
    }

    .main {
        margin-left: 0;
    }

    .mobile-menu {
        display: block;
        margin-right: 12px;
    }

    .topbar {
        padding: 0 15px;
    }

    .content {
        padding: 18px;
    }

    .cards {
        grid-template-columns: 1fr;
    }

    .section-header {
        flex-direction: column;
        align-items: stretch;
        gap: 12px;
    }

    .form-grid {
        grid-template-columns: 1fr;
    }

    .full {
        grid-column: auto;
    }

    .user strong,
    .user small {
        display: none;
    }

}
</style>
</head>

<body>

<!-- MENU LATERAL -->

<aside class="sidebar" id="sidebar">

    <div class="logo">
        🛶 canoa <span>teste</span>
    </div>

    <div class="menu-title">
        Gestão
    </div>

    <div class="menu">

        <button class="active" onclick="abrirSecao('dashboard', this)">
            <span class="icon">📊</span>
            Dashboard
        </button>

        <button onclick="abrirSecao('canoas', this)">
            <span class="icon">🛶</span>
            Canoas
        </button>

        <button onclick="abrirSecao('movimentacao', this)">
            <span class="icon">🔄</span>
            Entrada e Saída
        </button>

        <button onclick="abrirSecao('clientes', this)">
            <span class="icon">👥</span>
            Clientes
        </button>

        <button onclick="abrirSecao('localizacao', this)">
            <span class="icon">📍</span>
            Localização
        </button>

        <button onclick="abrirSecao('manutencao', this)">
            <span class="icon">🔧</span>
            Manutenção
        </button>

        <button onclick="abrirSecao('historico', this)">
            <span class="icon">🕐</span>
            Histórico
        </button>

    </div>

    <div class="menu-title">
        Sistema
    </div>

    <div class="menu">

        <button onclick="alert('Área de configurações')">
            <span class="icon">⚙️</span>
            Configurações
        </button>

    </div>

</aside>


<!-- CONTEÚDO -->

<main class="main">

    <header class="topbar">

        <div style="display:flex;align-items:center">

            <button class="mobile-menu"
                    onclick="toggleMenu()">
                ☰
            </button>

            <div class="topbar-title"
                 id="pageTitle">
                Dashboard
            </div>

        </div>

        <div class="user">

            <div>
                <strong>Administrador</strong>
                <small style="display:block;color:#718096">
                    Gestor
                </small>
            </div>

            <div class="avatar">
                AD
            </div>

        </div>

    </header>


    <div class="content">


        <!-- DASHBOARD -->

        <section class="section active"
                 id="dashboard">

            <div class="cards">

                <div class="card stat">

                    <div>
                        <p>Total de canoas</p>
                        <h3 id="totalCanoas">0</h3>
                    </div>

                    <div class="stat-icon blue">
                        🛶
                    </div>

                </div>


                <div class="card stat">

                    <div>
                        <p>Disponíveis</p>
                        <h3 id="totalDisponiveis">0</h3>
                    </div>

                    <div class="stat-icon green">
                        ✓
                    </div>

                </div>


                <div class="card stat">

                    <div>
                        <p>Em uso</p>
                        <h3 id="totalUso">0</h3>
                    </div>

                    <div class="stat-icon yellow">
                        🚣
                    </div>

                </div>


                <div class="card stat">

                    <div>
                        <p>Manutenção</p>
                        <h3 id="totalManutencao">0</h3>
                    </div>

                    <div class="stat-icon red">
                        🔧
                    </div>

                </div>

            </div>


            <div class="dashboard-grid">

                <div class="card">

                    <div class="section-header">

                        <h2>Canoas em circulação</h2>

                        <button class="btn btn-secondary"
                                onclick="abrirPorNome('movimentacao')">
                            Ver todas
                        </button>

                    </div>

                    <div class="table-container">

                        <table>

                            <thead>
                                <tr>
                                    <th>Canoa</th>
                                    <th>Cliente</th>
                                    <th>Saída</th>
                                    <th>Entrada prevista</th>
                                    <th>Status</th>
                                </tr>
                            </thead>

                            <tbody id="dashboardMovimentacoes"></tbody>

                        </table>

                    </div>

                </div>


                <div class="card">

                    <div class="section-header">
                        <h2>Atividades recentes</h2>
                    </div>

                    <ul class="activity">

                        <li>
                            <div class="activity-icon">
                                🛶
                            </div>

                            <div>
                                <strong>Canoa C-012 saiu</strong>
                                <small>
                                    João Silva · há 15 minutos
                                </small>
                            </div>
                        </li>

                        <li>
                            <div class="activity-icon">
                                ✓
                            </div>

                            <div>
                                <strong>Canoa C-008 entrou</strong>
                                <small>
                                    Maria Souza · há 35 minutos
                                </small>
                            </div>
                        </li>

                        <li>
                            <div class="activity-icon">
                                🔧
                            </div>

                            <div>
                                <strong>Canoa C-004 em manutenção</strong>
                                <small>
                                    há 1 hora
                                </small>
                            </div>
                        </li>

                    </ul>

                </div>

            </div>

        </section>


        <!-- CANOAS -->

        <section class="section"
                 id="canoas">

            <div class="section-header">

                <div>
                    <h2>Canoas</h2>

                    <p>
                        Cadastro e controle da frota.
                    </p>
                </div>

                <button class="btn btn-primary"
                        onclick="abrirModal('canoaModal')">
                    + Nova canoa
                </button>

            </div>


            <div class="search-box">

                <input
                    class="search"
                    id="buscarCanoa"
                    placeholder="🔎 Buscar canoa..."
                    oninput="renderizarCanoas()"
                >

            </div>


            <div class="table-container">

                <table>

                    <thead>

                        <tr>
                            <th>Código</th>
                            <th>Modelo</th>
                            <th>Capacidade</th>
                            <th>Localização</th>
                            <th>Status</th>
                            <th>Ação</th>
                        </tr>

                    </thead>

                    <tbody id="canoasTabela"></tbody>

                </table>

            </div>

        </section>


        <!-- ENTRADA E SAÍDA -->

        <section class="section"
                 id="movimentacao">

            <div class="section-header">

                <div>

                    <h2>Entrada e Saída</h2>

                    <p>
                        Controle de retirada e retorno das canoas.
                    </p>

                </div>

                <button class="btn btn-primary"
                        onclick="abrirModal('saidaModal')">
                    + Registrar saída
                </button>

            </div>


            <div class="table-container">

                <table>

                    <thead>

                        <tr>
                            <th>Canoa</th>
                            <th>Cliente</th>
                            <th>Telefone</th>
                            <th>Saída</th>
                            <th>Entrada prevista</th>
                            <th>Status</th>
                            <th>Ação</th>
                        </tr>

                    </thead>

                    <tbody id="movimentacoesTabela"></tbody>

                </table>

            </div>

        </section>


        <!-- CLIENTES -->

        <section class="section"
                 id="clientes">

            <div class="section-header">

                <div>

                    <h2>Clientes</h2>

                    <p>
                        Cadastro dos clientes da empresa.
                    </p>

                </div>

                <button class="btn btn-primary"
                        onclick="abrirModal('clienteModal')">
                    + Novo cliente
                </button>

            </div>


            <div class="table-container">

                <table>

                    <thead>

                        <tr>
                            <th>Nome</th>
                            <th>Documento</th>
                            <th>Telefone</th>
                            <th>Utilizações</th>
                            <th>Status</th>
                        </tr>

                    </thead>

                    <tbody id="clientesTabela"></tbody>

                </table>

            </div>

        </section>


        <!-- LOCALIZAÇÃO -->

        <section class="section"
                 id="localizacao">

            <div class="section-header">

                <div>

                    <h2>Localização</h2>

                    <p>
                        Localização registrada das canoas.
                    </p>

                </div>

            </div>


            <div class="card">

                <div class="map">

                    <div class="water"></div>

                    <div class="marker m1">
                        🛶 C-012
                    </div>

                    <div class="marker m2">
                        🛶 C-018
                    </div>

                    <div class="marker m3">
                        🛶 C-021
                    </div>

                    <div class="marker m4">
                        🛶 C-005
                    </div>

                </div>

            </div>

        </section>


        <!-- MANUTENÇÃO -->

        <section class="section"
                 id="manutencao">

            <div class="section-header">

                <div>

                    <h2>Manutenção</h2>

                    <p>
                        Controle de reparos e revisões.
                    </p>

                </div>

                <button class="btn btn-primary"
                        onclick="alert('Cadastro de manutenção')">
                    + Registrar manutenção
                </button>

            </div>


            <div class="table-container">

                <table>

                    <thead>

                        <tr>
                            <th>Canoa</th>
                            <th>Problema</th>
                            <th>Entrada</th>
                            <th>Responsável</th>
                            <th>Status</th>
                        </tr>

                    </thead>

                    <tbody>

                        <tr>

                            <td><strong>C-004</strong></td>

                            <td>Reparo no casco</td>

                            <td>08/09/2026</td>

                            <td>Oficina</td>

                            <td>
                                <span class="badge manutencao">
                                    Em manutenção
                                </span>
                            </td>

                        </tr>

                        <tr>

                            <td><strong>C-019</strong></td>

                            <td>Troca de assento</td>

                            <td>07/09/2026</td>

                            <td>Oficina</td>

                            <td>
                                <span class="badge manutencao">
                                    Em manutenção
                                </span>
                            </td>

                        </tr>

                    </tbody>

                </table>

            </div>

        </section>


        <!-- HISTÓRICO -->

        <section class="section"
                 id="historico">

            <div class="section-header">

                <div>

                    <h2>Histórico</h2>

                    <p>
                        Registro das movimentações.
                    </p>

                </div>

            </div>


            <div class="table-container">

                <table>

                    <thead>

                        <tr>
                            <th>Data</th>
                            <th>Canoa</th>
                            <th>Evento</th>
                            <th>Cliente</th>
                            <th>Responsável</th>
                        </tr>

                    </thead>

                    <tbody>

                        <tr>
                            <td>08/09/2026 18:40</td>
                            <td>C-008</td>
                            <td>Entrada</td>
                            <td>Maria Souza</td>
                            <td>Administrador</td>
                        </tr>

                        <tr>
                            <td>08/09/2026 18:15</td>
                            <td>C-012</td>
                            <td>Saída</td>
                            <td>João Silva</td>
                            <td>Administrador</td>
                        </tr>

                        <tr>
                            <td>08/09/2026 17:30</td>
                            <td>C-004</td>
                            <td>Manutenção</td>
                            <td>-</td>
                            <td>Administrador</td>
                        </tr>

                    </tbody>

                </table>

            </div>

        </section>


    </div>

</main>


<!-- MODAL NOVA CANOA -->

<div class="modal"
     id="canoaModal">

    <div class="modal-box">

        <div class="modal-header">

            <h2>Nova canoa</h2>

            <button class="close"
                    onclick="fecharModal('canoaModal')">
                ×
            </button>

        </div>


        <form onsubmit="cadastrarCanoa(event)">

            <div class="form-grid">

                <div class="form-group">

                    <label>Código</label>

                    <input
                        id="canoaCodigo"
                        placeholder="Ex.: C-025"
                        required
                    >

                </div>


                <div class="form-group">

                    <label>Modelo</label>

                    <input
                        id="canoaModelo"
                        placeholder="Ex.: Turismo"
                        required
                    >

                </div>


                <div class="form-group">

                    <label>Capacidade</label>

                    <select id="canoaCapacidade">

                        <option>1 pessoa</option>
                        <option>2 pessoas</option>
                        <option>3 pessoas</option>
                        <option>4 pessoas</option>
                        <option>5 pessoas</option>
                        <option>6 pessoas</option>

                    </select>

                </div>


                <div class="form-group">

                    <label>Localização</label>

                    <input
                        id="canoaLocalizacao"
                        value="Base principal"
                    >

                </div>


                <div class="form-group full">

                    <label>Observações</label>

                    <textarea
                        id="canoaObservacao">
                    </textarea>

                </div>

            </div>


            <div class="modal-footer">

                <button type="button"
                        class="btn btn-secondary"
                        onclick="fecharModal('canoaModal')">
                    Cancelar
                </button>

                <button class="btn btn-primary">
                    Cadastrar
                </button>

            </div>

        </form>

    </div>

</div>


<!-- MODAL SAÍDA -->

<div class="modal"
     id="saidaModal">

    <div class="modal-box">

        <div class="modal-header">

            <h2>Registrar saída</h2>

            <button class="close"
                    onclick="fecharModal('saidaModal')">
                ×
            </button>

        </div>


        <form onsubmit="registrarSaida(event)">

            <div class="form-grid">

                <div class="form-group full">

                    <label>Cliente</label>

                    <select id="saidaCliente"
                            required>
                    </select>

                </div>


                <div class="form-group">

                    <label>Canoa</label>

                    <select id="saidaCanoa"
                            required>
                    </select>

                </div>


                <div class="form-group">

                    <label>Quantidade de pessoas</label>

                    <input
                        type="number"
                        value="1"
                        min="1"
                        required
                    >

                </div>


                <div class="form-group">

                    <label>Data e hora da saída</label>

                    <input
                        type="datetime-local"
                        id="saidaData"
                        required
                    >

                </div>


                <div class="form-group">

                    <label>Entrada prevista</label>

                    <input
                        type="datetime-local"
                        id="entradaPrevista"
                        required
                    >

                </div>


                <div class="form-group">

                    <label>Valor</label>

                    <input
                        type="number"
                        step="0.01"
                        placeholder="0,00"
                    >

                </div>


                <div class="form-group">

                    <label>Forma de pagamento</label>

                    <select>

                        <option>Pix</option>
                        <option>Dinheiro</option>
                        <option>Cartão</option>
                        <option>Não pago</option>

                    </select>

                </div>


                <div class="form-group full">

                    <label>Observações</label>

                    <textarea
                        placeholder="Informações da saída...">
                    </textarea>

                </div>

            </div>


            <div class="modal-footer">

                <button type="button"
                        class="btn btn-secondary"
                        onclick="fecharModal('saidaModal')">
                    Cancelar
                </button>

                <button class="btn btn-primary">
                    Registrar saída
                </button>

            </div>

        </form>

    </div>

</div>


<!-- MODAL CLIENTE -->

<div class="modal"
     id="clienteModal">

    <div class="modal-box">

        <div class="modal-header">

            <h2>Novo cliente</h2>

            <button class="close"
                    onclick="fecharModal('clienteModal')">
                ×
            </button>

        </div>


        <form onsubmit="cadastrarCliente(event)">

            <div class="form-grid">

                <div class="form-group full">

                    <label>Nome completo</label>

                    <input
                        id="clienteNome"
                        required
                    >

                </div>


                <div class="form-group">

                    <label>CPF / Documento</label>

                    <input
                        id="clienteDocumento"
                    >

                </div>


                <div class="form-group">

                    <label>Telefone</label>

                    <input
                        id="clienteTelefone"
                    >

                </div>


                <div class="form-group full">

                    <label>E-mail</label>

                    <input
                        type="email"
                        id="clienteEmail"
                    >

                </div>

            </div>


            <div class="modal-footer">

                <button type="button"
                        class="btn btn-secondary"
                        onclick="fecharModal('clienteModal')">
                    Cancelar
                </button>

                <button class="btn btn-primary">
                    Cadastrar cliente
                </button>

            </div>

        </form>

    </div>

</div>


<script>

/* ==============================
   DADOS INICIAIS
============================== */

let canoas = JSON.parse(
    localStorage.getItem("canoa_teste_canoas")
) || [

    {
        codigo: "C-001",
        modelo: "Canadense",
        capacidade: "2 pessoas",
        localizacao: "Base principal",
        status: "Disponível"
    },

    {
        codigo: "C-004",
        modelo: "Turismo",
        capacidade: "3 pessoas",
        localizacao: "Oficina",
        status: "Manutenção"
    },

    {
        codigo: "C-008",
        modelo: "Esportiva",
        capacidade: "2 pessoas",
        localizacao: "Base principal",
        status: "Disponível"
    },

    {
        codigo: "C-012",
        modelo: "Turismo",
        capacidade: "4 pessoas",
        localizacao: "Rio",
        status: "Em uso"
    },

    {
        codigo: "C-018",
        modelo: "Canadense",
        capacidade: "3 pessoas",
        localizacao: "Rio",
        status: "Em uso"
    },

    {
        codigo: "C-021",
        modelo: "Esportiva",
        capacidade: "2 pessoas",
        localizacao: "Rio",
        status: "Em uso"
    }

];


let clientes = JSON.parse(
    localStorage.getItem("canoa_teste_clientes")
) || [

    {
        nome: "João Silva",
        documento: "123.456.789-00",
        telefone: "(27) 99999-1111",
        email: "joao@email.com",
        utilizacoes: 8
    },

    {
        nome: "Maria Souza",
        documento: "987.654.321-00",
        telefone: "(27) 98888-2222",
        email: "maria@email.com",
        utilizacoes: 4
    },

    {
        nome: "Pedro Oliveira",
        documento: "456.789.123-00",
        telefone: "(27) 97777-3333",
        email: "pedro@email.com",
        utilizacoes: 2
    }

];


let movimentacoes = [

    {
        canoa: "C-012",
        cliente: "João Silva",
        telefone: "(27) 99999-1111",
        saida: "18:15",
        entrada: "20:30",
        status: "Em uso"
    },

    {
        canoa: "C-018",
        cliente: "Maria Souza",
        telefone: "(27) 98888-2222",
        saida: "17:50",
        entrada: "20:00",
        status: "Em uso"
    },

    {
        canoa: "C-021",
        cliente: "Pedro Oliveira",
        telefone: "(27) 97777-3333",
        saida: "18:30",
        entrada: "21:00",
        status: "Em uso"
    }

];


/* ==============================
   NAVEGAÇÃO
============================== */

const titulos = {

    dashboard: "Dashboard",
    canoas: "Canoas",
    movimentacao: "Entrada e Saída",
    clientes: "Clientes",
    localizacao: "Localização",
    manutencao: "Manutenção",
    historico: "Histórico"

};


function abrirSecao(id, botao) {

    document
        .querySelectorAll(".section")
        .forEach(secao =>
            secao.classList.remove("active")
        );

    document
        .getElementById(id)
        .classList.add("active");


    document
        .querySelectorAll(".menu button")
        .forEach(btn =>
            btn.classList.remove("active")
        );


    if(botao) {
        botao.classList.add("active");
    }


    document.getElementById(
        "pageTitle"
    ).textContent = titulos[id];


    document
        .getElementById("sidebar")
        .classList.remove("open");

}


function abrirPorNome(id) {

    const botao =
        [...document.querySelectorAll(".menu button")]
        .find(btn =>
            btn.getAttribute("onclick")?.includes(
                "'" + id + "'"
            )
        );

    abrirSecao(id, botao);

}


function toggleMenu() {

    document
        .getElementById("sidebar")
        .classList.toggle("open");

}


/* ==============================
   MODAIS
============================== */

function abrirModal(id) {

    if(id === "saidaModal") {

        carregarClientes();

        carregarCanoasDisponiveis();

    }

    document
        .getElementById(id)
        .classList.add("show");

}


function fecharModal(id) {

    document
        .getElementById(id)
        .classList.remove("show");

}


window.onclick = function(event) {

    if(
        event.target.classList.contains("modal")
    ) {

        event.target.classList.remove("show");

    }

};


/* ==============================
   CANOAS
============================== */

function classeStatus(status) {

    if(status === "Disponível")
        return "disponivel";

    if(status === "Em uso")
        return "em-uso";

    if(status === "Reservada")
        return "reservada";

    return "manutencao";

}


function renderizarCanoas() {

    const tabela =
        document.getElementById("canoasTabela");

    const busca =
        document
            .getElementById("buscarCanoa")
            ?.value
            .toLowerCase() || "";


    tabela.innerHTML = "";


    canoas
        .filter(c =>
            c.codigo.toLowerCase().includes(busca) ||
            c.modelo.toLowerCase().includes(busca) ||
            c.localizacao.toLowerCase().includes(busca)
        )
        .forEach(c => {

            tabela.innerHTML += `

                <tr>

                    <td>
                        <strong>${c.codigo}</strong>
                    </td>

                    <td>${c.modelo}</td>

                    <td>${c.capacidade}</td>

                    <td>
                        📍 ${c.localizacao}
                    </td>

                    <td>

                        <span class="badge ${classeStatus(c.status)}">
                            ${c.status}
                        </span>

                    </td>

                    <td>

                        <button
                            class="btn btn-secondary"
                            onclick="verCanoa('${c.codigo}')">
                            Ver
                        </button>

                    </td>

                </tr>

            `;

        });


    atualizarDashboard();

}


function cadastrarCanoa(event) {

    event.preventDefault();


    const codigo =
        document.getElementById("canoaCodigo").value.trim();


    if(
        canoas.some(c => c.codigo === codigo)
    ) {

        alert("Já existe uma canoa com esse código.");

        return;

    }


    canoas.push({

        codigo,

        modelo:
            document.getElementById("canoaModelo").value,

        capacidade:
            document.getElementById("canoaCapacidade").value,

        localizacao:
            document.getElementById("canoaLocalizacao").value,

        status: "Disponível"

    });


    salvarDados();

    renderizarCanoas();

    fecharModal("canoaModal");

    event.target.reset();

    alert("Canoa cadastrada com sucesso!");

}


function verCanoa(codigo) {

    const c =
        canoas.find(c => c.codigo === codigo);


    alert(

        "CANOA\n\n" +

        "Código: " + c.codigo + "\n" +

        "Modelo: " + c.modelo + "\n" +

        "Capacidade: " + c.capacidade + "\n" +

        "Localização: " + c.localizacao + "\n" +

        "Status: " + c.status

    );

}


/* ==============================
   DASHBOARD
============================== */

function atualizarDashboard() {

    document.getElementById(
        "totalCanoas"
    ).textContent = canoas.length;


    document.getElementById(
        "totalDisponiveis"
    ).textContent =
        canoas.filter(
            c => c.status === "Disponível"
        ).length;


    document.getElementById(
        "totalUso"
    ).textContent =
        canoas.filter(
            c => c.status === "Em uso"
        ).length;


    document.getElementById(
        "totalManutencao"
    ).textContent =
        canoas.filter(
            c => c.status === "Manutenção"
        ).length;


    renderizarDashboardMovimentacoes();

}


function renderizarDashboardMovimentacoes() {

    const tabela =
        document.getElementById(
            "dashboardMovimentacoes"
        );

    tabela.innerHTML = "";


    movimentacoes
        .slice(0,5)
        .forEach(m => {

            tabela.innerHTML += `

                <tr>

                    <td>
                        <strong>${m.canoa}</strong>
                    </td>

                    <td>${m.cliente}</td>

                    <td>${m.saida}</td>

                    <td>${m.entrada}</td>

                    <td>
                        <span class="badge em-uso">
                            ${m.status}
                        </span>
                    </td>

                </tr>

            `;

        });

}


/* ==============================
   ENTRADA / SAÍDA
============================== */

function carregarClientes() {

    const select =
        document.getElementById(
            "saidaCliente"
        );

    select.innerHTML =
        '<option value="">Selecione...</option>';


    clientes.forEach(c => {

        select.innerHTML += `

            <option value="${c.nome}">
                ${c.nome}
            </option>

        `;

    });

}


function carregarCanoasDisponiveis() {

    const select =
        document.getElementById(
            "saidaCanoa"
        );

    select.innerHTML =
        '<option value="">Selecione...</option>';


    canoas
        .filter(c =>
            c.status === "Disponível"
        )
        .forEach(c => {

            select.innerHTML += `

                <option value="${c.codigo}">
                    ${c.codigo} - ${c.modelo}
                </option>

            `;

        });

}


function renderizarMovimentacoes() {

    const tabela =
        document.getElementById(
            "movimentacoesTabela"
        );

    tabela.innerHTML = "";


    movimentacoes.forEach(
        (m, index) => {

            tabela.innerHTML += `

                <tr>

                    <td>
                        <strong>${m.canoa}</strong>
                    </td>

                    <td>${m.cliente}</td>

                    <td>${m.telefone}</td>

                    <td>${m.saida}</td>

                    <td>${m.entrada}</td>

                    <td>

                        <span class="badge em-uso">
                            ${m.status}
                        </span>

                    </td>

                    <td>

                        <button
                            class="btn btn-primary"
                            onclick="registrarEntrada(${index})">
                            Registrar entrada
                        </button>

                    </td>

                </tr>

            `;

        }
    );

}


function registrarSaida(event) {

    event.preventDefault();


    const canoaCodigo =
        document.getElementById(
            "saidaCanoa"
        ).value;


    const clienteNome =
        document.getElementById(
            "saidaCliente"
        ).value;


    const cliente =
        clientes.find(
            c => c.nome === clienteNome
        );


    const dataSaida =
        document.getElementById(
            "saidaData"
        ).value;


    const dataEntrada =
        document.getElementById(
            "entradaPrevista"
        ).value;


    if(
        !canoaCodigo ||
        !clienteNome
    ) {

        alert(
            "Selecione a canoa e o cliente."
        );

        return;

    }


    movimentacoes.push({

        canoa: canoaCodigo,

        cliente: clienteNome,

        telefone:
            cliente?.telefone || "-",

        saida:
            formatarData(dataSaida),

        entrada:
            formatarData(dataEntrada),

        status: "Em uso"

    });


    const canoa =
        canoas.find(
            c => c.codigo === canoaCodigo
        );


    if(canoa) {

        canoa.status = "Em uso";

        canoa.localizacao = "Em uso";

    }


    if(cliente) {

        cliente.utilizacoes++;

    }


    salvarDados();

    renderizarCanoas();

    renderizarMovimentacoes();

    fecharModal("saidaModal");

    event.target.reset();

    alert(
        "Saída registrada com sucesso!"
    );

}


function registrarEntrada(index) {

    const movimentacao =
        movimentacoes[index];


    if(
        !confirm(
            "Registrar entrada da canoa " +
            movimentacao.canoa +
            "?"
        )
    ) return;


    const canoa =
        canoas.find(
            c => c.codigo === movimentacao.canoa
        );


    if(canoa) {

        canoa.status = "Disponível";

        canoa.localizacao =
            "Base principal";

    }


    movimentacoes.splice(index,1);


    salvarDados();

    renderizarCanoas();

    renderizarMovimentacoes();


    alert(
        "Entrada registrada com sucesso!"
    );

}


/* ==============================
   CLIENTES
============================== */

function renderizarClientes() {

    const tabela =
        document.getElementById(
            "clientesTabela"
        );

    tabela.innerHTML = "";


    clientes.forEach(c => {

        tabela.innerHTML += `

            <tr>

                <td>
                    <strong>${c.nome}</strong>
                </td>

                <td>${c.documento}</td>

                <td>${c.telefone}</td>

                <td>${c.utilizacoes}</td>

                <td>

                    <span class="badge disponivel">
                        Ativo
                    </span>

                </td>

            </tr>

        `;

    });

}


function cadastrarCliente(event) {

    event.preventDefault();


    clientes.push({

        nome:
            document.getElementById(
                "clienteNome"
            ).value,

        documento:
            document.getElementById(
                "clienteDocumento"
            ).value,

        telefone:
            document.getElementById(
                "clienteTelefone"
            ).value,

        email:
            document.getElementById(
                "clienteEmail"
            ).value,

        utilizacoes: 0

    });


    salvarDados();

    renderizarClientes();

    fecharModal("clienteModal");

    event.target.reset();


    alert(
        "Cliente cadastrado com sucesso!"
    );

}


/* ==============================
   UTILIDADES
============================== */

function formatarData(valor) {

    if(!valor)
        return "-";


    const data =
        new Date(valor);


    return data.toLocaleString(
        "pt-BR",
        {
            day: "2-digit",
            month: "2-digit",
            hour: "2-digit",
            minute: "2-digit"
        }
    );

}


function salvarDados() {

    localStorage.setItem(
        "canoa_teste_canoas",
        JSON.stringify(canoas)
    );


    localStorage.setItem(
        "canoa_teste_clientes",
        JSON.stringify(clientes)
    );

}


/* ==============================
   INICIALIZAÇÃO
============================== */

function iniciar() {

    renderizarCanoas();

    renderizarMovimentacoes();

    renderizarClientes();

    atualizarDashboard();

}


iniciar();

</script>

</body>
</html>
