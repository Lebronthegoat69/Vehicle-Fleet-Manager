using System;
using System.Collections.Generic;
using System.Linq;

public class Fleet
{
    private List<Vehicle> _vehicles = new List<Vehicle>();

    public void AddVehicle(Vehicle v)
    {
        _vehicles.Add(v);
    }

    public void RemoveVehicle(string model)
    {
        _vehicles.RemoveAll(v => v.Model.Equals(model, StringComparison.OrdinalIgnoreCase));
    }

    public double GetAverageMileage()
    {
        if (_vehicles.Count == 0)
            return 0;

        return _vehicles.Average(v => v.Mileage);
    }

    public void DisplayAllVehicles()
    {
        if (_vehicles.Count == 0)
        {
            Console.WriteLine("No vehicles in fleet.");
            return;
        }

        foreach (var vehicle in _vehicles)
        {
            Console.WriteLine(vehicle.GetSummary());
        }
    }

    public void ServiceAllDue()
    {
        int count = 0;

        foreach (var vehicle in _vehicles)
        {
            if (vehicle.NeedsService())
            {
                vehicle.PerformService();
                count++;
            }
        }

        Console.WriteLine($"{count} vehicles serviced.");
    }
}
