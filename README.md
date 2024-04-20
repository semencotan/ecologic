# ecologic
def calculate_carbon_footprint(driving_distance, electricity_consumption, waste_production):
    """
    Calculate carbon footprint.

    Args:
    driving_distance: The distance driven in kilometers per month.
    electricity_consumption: The monthly electricity consumption in kWh.
    waste_production: The monthly waste production in kilograms.

    Returns:
    The carbon footprint in kilograms of CO2 equivalent.
    """
    # Carbon emission factors (kgCO2eq per unit)
    driving_emission_factor = 0.2  # kgCO2eq per km
    electricity_emission_factor = 0.5  # kgCO2eq per kWh
    waste_emission_factor = 0.1  # kgCO2eq per kg

    # Calculate carbon footprint
    driving_emissions = driving_distance * driving_emission_factor
    electricity_emissions = electricity_consumption * electricity_emission_factor
    waste_emissions = waste_production * waste_emission_factor

    total_emissions = driving_emissions + electricity_emissions + waste_emissions
    return total_emissions

# Example usage:
driving_distance_km = 500  # km driven per month
electricity_consumption_kWh = 200  # kWh consumed per month
waste_production_kg = 50  # kg of waste produced per month

carbon_footprint = calculate_carbon_footprint(driving_distance_km, electricity_consumption_kWh, waste_production_kg)
print("Carbon footprint:", carbon_footprint, "kgCO2eq")
