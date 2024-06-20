using System;
using System.Collections.Generic;

namespace TaxiParks
{
    // Класс для хранения информации о таксопарке
    public class TaxiPark
    {
        public string Name { get; set; }
        public string Location { get; set; }

        // Конструктор для инициализации данных таксопарка
        public TaxiPark(string name, string location)
        {
            Name = name;
            Location = location;
        }
    }

    class Program
    {
        static void Main(string[] args)
        {
            // Список таксопарков в Тирасполе
            List<TaxiPark> taxiParks = new List<TaxiPark>
            {
                new TaxiPark("Тираспольский таксопарк №1", "ул. Ленина, 15"),
                new TaxiPark("Такси Тирасполь", "ул. Карла Маркса, 22"),
                new TaxiPark("Таксопарк Приднестровья", "ул. Октябрьская, 7")
            };

            // Вывод информации о таксопарках
            Console.WriteLine("Таксопарки в Тирасполе:");
            foreach (var taxiPark in taxiParks)
            {
                Console.WriteLine($"Название: {taxiPark.Name}, Местоположение: {taxiPark.Location}");
            }
        }
    }
}
