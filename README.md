# Prova do neri

string nomePrimeiroItem = "Câmara de ar", nomeSegundoItem = "Capacete", nomeTerceiroItem = "Kit de Ferramentas";
double precoPrimeiroItem = 29.90, precoSegundoItem = 134.90, precoTerceiroItem = 189.90;
double percentualImpostoVenda = 0.088;

Console.WriteLine("\n------------------ Bem-Vindo(a) a Oficina BikePro ------------------\n");

Console.WriteLine("+==================================================================+");
Console.WriteLine("|                          Oficina BikePro                         |");
Console.WriteLine("+==================================================================+");
Console.WriteLine("|                             CATALOGO                             |");
Console.WriteLine("+==================================================================+");
Console.WriteLine("|            ITEM                                   VALOR          |");
Console.WriteLine("+==================================================================+");
Console.WriteLine($"|  1. {nomePrimeiroItem.ToUpper().PadRight(43)}  {precoPrimeiroItem:C2}        |");
Console.WriteLine($"|  1. {nomeSegundoItem.ToUpper().PadRight(43)}  {precoSegundoItem:C2}       |");
Console.WriteLine($"|  1. {nomeTerceiroItem.ToUpper().PadRight(43)}  {precoTerceiroItem:C2}       |");
Console.WriteLine("+==================================================================+");  
Console.WriteLine($"|  Imposto sobre a venda: {percentualImpostoVenda.ToString("P1").PadRight(41)}|");
Console.WriteLine("+==================================================================+");

Console.ReadKey();
Console.Clear();

Console.Write($"Digite a quantidade que você deseja de {nomePrimeiroItem}: ");
int qtdItem1 = int.Parse(Console.ReadLine()!);
Console.Write($"Digite a quantidade que você deseja de {nomeSegundoItem}: ");
int qtdItem2 = int.Parse(Console.ReadLine()!);
Console.Write($"Digite a quantidade que você deseja de {nomeTerceiroItem}: ");
int qtdItem3 = int.Parse(Console.ReadLine()!);

Console.Clear();

precoPrimeiroItem *= qtdItem1;
precoSegundoItem *= qtdItem2;
precoTerceiroItem *= qtdItem3;

double totalPrimeiroCliente = precoPrimeiroItem + precoSegundoItem + precoTerceiroItem;
double impostoPrimeiroCliente = totalPrimeiroCliente * percentualImpostoVenda;
double ValorFinalPrimeiroCliente = totalPrimeiroCliente + impostoPrimeiroCliente;

Console.WriteLine("+==================================================================+");
Console.WriteLine("|                          RECIBO DE COMPRA                        |");
Console.WriteLine("+==================================================================+");
Console.WriteLine("|       ITEM                                          VALOR        |");
Console.WriteLine("+==================================================================+");
Console.WriteLine($"| {qtdItem1}x {nomePrimeiroItem.ToUpper().PadRight(45)} {precoPrimeiroItem:C2}        |");
Console.WriteLine($"| {qtdItem2}x {nomeSegundoItem.ToUpper().PadRight(45)} {precoSegundoItem:C2}       |");
Console.WriteLine($"| {qtdItem3}x {nomeTerceiroItem.ToUpper().PadRight(45)} {precoTerceiroItem:C2}       |");
Console.WriteLine("+==================================================================+");
Console.WriteLine($"|                               IMPOSTO ({percentualImpostoVenda.ToString("P1")}): {impostoPrimeiroCliente:C2}           |");
Console.WriteLine("+==================================================================+");
Console.WriteLine($"|                                         TOTAL: {ValorFinalPrimeiroCliente:C2}         |");
Console.WriteLine("+==================================================================+");
