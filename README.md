# ระบบบันทึกข้อมูลข้าวโพด (Corn Yield Recording System)

## Objective
This application helps farmers and agricultural officers record and analyze corn yield data. It calculates the yield per area (Yield Estimate) based on the actual harvest weight and the planting area, allowing for efficient data management and analysis.

## How it Works
The application is a web-based form built with React and styled with Tailwind CSS. It allows users to input the following data:

1.  **Species (สายพันธุ์ข้าวโพด)**: Select the corn species from a predefined list (e.g., #71, #51, #55).
2.  **Zone (เขตพื้นที่)**: Select the agricultural zone (e.g., NMA, CPM, SKT).
3.  **Grade (เกรด)**: Select the quality grade of the corn (e.g., GF, GF1, YF).
4.  **Plan (แผน - ตัน)**: Enter the planned harvest amount in tons.
5.  **Actual (เข้าจริง - ตัน)**: Enter the actually harvested amount in tons.
6.  **Area (จำนวนไร่)**: Enter the planting area size in Rai.

### Calculation Logic
The system automatically calculates the yield per Rai when the "Actual" harvest and "Area" are provided:

$$ \text{Yield (kg/Rai)} = \frac{\text{Actual Harvest (Tons)} \times 1000}{\text{Area (Rai)}} $$

### Data Submission
Upon clicking "บันทึกข้อมูล" (Save Data), the system simulates sending the data to a Google Apps Script endpoint (currently mocked for demonstration or ready for integration). It displays a success message upon completion.