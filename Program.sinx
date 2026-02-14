using System;

class Program
{
    static void Main()
    {
        Fleet fleet = new Fleet();
        bool running = true;

        while (running)
        {
            Console.WriteLine("\n=== Vehicle Fleet Manager ===");
            Console.WriteLine("1. Add Vehicle");
            Console.WriteLine("2. Remove Vehicle");
            Console.WriteLine("3. Display Fleet");
            Console.WriteLine("4. Show Average Mileage");
            Console.WriteLine("5. Service Due Vehicles");
            Console.WriteLine("6. Exit");
            Console.Write("Choose: ");

            string choice = Console.ReadLine();

            switch (choice)
            {
                case "1":
                    Console.Write("Enter Make: ");
                    string make = Console.ReadLine();

                    Console.Write("Enter Model: ");
                    string model = Console.ReadLine();

                    Console.Write("Enter Year: ");
                    int year = int.Parse(Console.ReadLine());

                    Console.Write("Enter Mileage: ");
                    double mileage = double.Parse(Console.ReadLine());

                    Vehicle v = new Vehicle(make, model, year, mileage);
                    fleet.AddVehicle(v);

                    Console.WriteLine("Vehicle added!");
                    break;

                case "2":
                    Console.Write("Enter Model to remove: ");
                    string removeModel = Console.ReadLine();
                    fleet.RemoveVehicle(removeModel);
                    Console.WriteLine("Vehicle(s) removed.");
                    break;

                case "3":
                    fleet.DisplayAllVehicles();
                    break;

                case "4":
                    Console.WriteLine($"Average Mileage: {fleet.GetAverageMileage()}");
                    break;

                case "5":
                    fleet.ServiceAllDue();
                    break;

                case "6":
                    running = false;
                    break;

                default:
                    Console.WriteLine("Invalid choice.");
                    break;
            }
        }
    }
}
