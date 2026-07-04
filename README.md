<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Notas Fiscais - Gerenciamento</title>
    <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Inter', sans-serif; }
    </style>
</head>
<body class="bg-[#F4F5F7] p-6 text-[#333333]">

    <div class="max-w-7xl mx-auto">
        
        <div class="flex justify-between items-center mb-6">
            <div>
                <h1 class="text-2xl font-bold flex items-center gap-2">
                    📋 Notas Fiscais
                </h1>
                <p class="text-sm text-gray-500">Gerenciamento de recebimento</p>
            </div>
            <div class="flex gap-3">
                <button class="bg-white border border-gray-300 text-gray-700 px-4 py-2 rounded-lg font-medium shadow-sm hover:bg-gray-50 transition flex items-center gap-2 text-sm">
                    ⬇️ Exportar CSV
                </button>
                <button class="bg-[#2B59C3] text-white px-4 py-2 rounded-lg font-medium shadow-sm hover:bg-[#22479D] transition text-sm">
                    + Nova Nota Fiscal
                </button>
            </div>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-4 gap-4 mb-6">
            <div class="bg-white p-4 rounded-xl border border-gray-200 shadow-xs">
                <p class="text-xs font-semibold text-gray-400 uppercase tracking-wider">Total de Notas</p>
                <p class="text-2xl font-bold text-[#2B59C3] mt-1" id="card-total-notas">6</p>
            </div>
            <div class="bg-white p-4 rounded-xl border border-gray-200 shadow-xs">
                <p class="text-xs font-semibold text-gray-400 uppercase tracking-wider">Valor Total</p>
                <p class="text-2xl font-bold text-gray-900 mt-1" id="card-valor-total">R$ 21.306,96</p>
            </div>
            <div class="bg-white p-4 rounded-xl border border-gray-200 shadow-xs">
                <p class="text-xs font-semibold text-gray-400 uppercase tracking-wider">Não Acatadas</p>
                <p class="text-2xl font-bold text-[#D34545] mt-1" id="card-nao-acatadas">6</p>
            </div>
            <div class="bg-white p-4 rounded-xl border border-gray-200 shadow-xs">
                <p class="text-xs font-semibold text-gray-400 uppercase tracking-wider">Acatadas</p>
                <p class="text-2xl font-bold text-[#2E7D32] mt-1" id="card-acatadas">0</p>
            </div>
        </div>

        <div class="bg-white rounded-xl border border-gray-200 shadow-xs p-4 mb-6 flex justify-between items-center">
            <button class="text-sm font-medium text-gray-700 flex items-center gap-2">
                ▼ Filtros
            </button>
            <button class="text-sm text-gray-500 border border-gray-300 px-3 py-1 rounded-lg hover:bg-gray-50">
                ✕ Limpar filtros
            </button>
        </div>

        <div class="bg-white rounded-xl border border-gray-200 shadow-xs overflow-hidden">
            <div class="p-4 border-b border-gray-100 bg-white">
                <p class="text-sm font-semibold text-gray-700" id="contador-linhas">6 notas encontradas</p>
                <p class="text-xs text-gray-400 mt-0.5">≡ Arraste os cabeçalhos para reordenar as colunas</p>
            </div>

            <div class="overflow-x-auto">
                <table class="w-full text-left border-collapse text-sm">
                    <thead>
                        <tr class="bg-[#F8F9FA] text-gray-500 font-medium border-b border-gray-200 text-xs">
                            <th class="p-3 pl-6">Data ↕</th>
                            <th class="p-3">Fornecedor ↕</th>
                            <th class="p-3">NF ↕</th>
                            <th class="p-3">Valor ↕</th>
                            <th class="p-3">Chegada</th>
                            <th class="p-3">Saída</th>
                            <th class="p-3">Temp.</th>
                            <th class="p-3">Conferente ↕</th>
                            <th class="p-3">Prevenção</th>
                            <th class="p-3">Status ↕</th>
                            <th class="p-3">Observação</th>
                            <th class="p-3 pr-6 text-center">Ações</th>
                        </tr>
                    </thead>
                    <tbody id="tabela-corpo" class="text-gray-700 divide-y divide-gray-100">
                        <tr class="hover:bg-gray-50 transition">
                            <td class="p-3 pl-6">22/06/2026</td>
                            <td class="p-3 font-medium">Pepsico</td>
                            <td class="p-3 text-gray-500">282.275</td>
                            <td class="p-3 font-semibold">R$ 28,65</td>
                            <td class="p-3">09:05</td>
                            <td class="p-3">10:53</td>
                            <td class="p-3 text-gray-400">-</td>
                            <td class="p-3 text-gray-400">-</td>
                            <td class="p-3 text-gray-400">-</td>
                            <td class="p-3"><span class="bg-[#FEE4E2] text-[#D34545] text-xs font-semibold px-2 py-1 rounded">NÃO ACATADA</span></td>
                            <td class="p-3 text-gray-400">-</td>
                            <td class="p-3 pr-6 text-center">
                                <button class="text-blue-600 hover:text-blue-800 mr-2">✏️</button>
                                <button class="text-red-600 hover:text-red-800">🗑️</button>
                            </td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>

    </div>

    <script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
    <script>
        // O código de conexão com o banco entrará aqui depois!
    </script>
</body>
</html>
