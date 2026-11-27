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



關卡設計（難度調整）
這次我調整了三個主要參數，分別是物件掉落速度、物件產生速度以及炸彈比例，希望讓遊戲隨著時間逐漸變得更刺激。在遊戲開始時，我把物件產生間隔設為 1.0 秒，掉落速度設為 -0.03，炸彈比例設為 20%，讓玩家一開始可以先熟悉操作。之後隨著剩餘時間變少，物件會產生得更快，掉落速度也會增加，同時炸彈比例提高。例如中段會將產生間隔縮短為 0.8 秒或 0.5 秒，掉落速度提高到 -0.04、-0.05，炸彈比例則提高到 40% 或 60%。這樣玩家需要更快判斷物品的位置，也要避免接到炸彈。最後幾秒我將產生間隔縮短到 0.3 秒，掉落速度提高到 -0.06，讓畫面上的物品快速增加，增加遊戲最後階段的緊張感。透過這些參數的調整，可以讓遊戲難度不是固定的，而是會隨著遊戲進行逐漸提高。
