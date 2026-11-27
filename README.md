# 151VR-HW6-414261668-CYX
if (this.time < 0)
{
    this.time = 0;

    this.generator.GetComponent<ItemGenerator>().SetParameter(
        10000.0f, 0, 0);
}
else if (0 <= this.time && this.time < 4)
{
    this.generator.GetComponent<ItemGenerator>().SetParameter(
        0.3f, -0.06f, 0);
}
else if (4 <= this.time && this.time < 12)
{
    this.generator.GetComponent<ItemGenerator>().SetParameter(
        0.5f, -0.05f, 6);
}
else if (12 <= this.time && this.time < 23)
{
    this.generator.GetComponent<ItemGenerator>().SetParameter(
        0.8f, -0.04f, 4);
}
else if (23 <= this.time && this.time < 30)
{
    this.generator.GetComponent<ItemGenerator>().SetParameter(
        1.0f, -0.03f, 2);
}
