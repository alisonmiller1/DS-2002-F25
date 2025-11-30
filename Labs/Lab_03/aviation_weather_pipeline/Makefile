.PHONY: all fetch analyze clean

all: analyze

fetch:
	@echo "---Fetching data---"
	./fetch_metars.sh
	@echo "---Fetch complete. Data stored in raw_metars."

analyze: fetch
	@echo "---Beginning analyze---"
	./analyze_data.sh
	@echo "Analyze complete. Data stored in weather_reports.csv"
	@echo "Pipeline complete."

clean:
	@echo "---Cleaning up---"
	rm -rf raw_metars weather_report.csv
	@echo "---Cleaned---"
