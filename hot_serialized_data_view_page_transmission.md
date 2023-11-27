Transmit the data via dictionary
````
for loss in losses:
    losses_data.append(
        {
            "id": loss.pk,
            "name": loss.name if loss.name else "Loss",
            "date": loss.accident_date.strftime("%d/%m/%Y"),
            "size": loss.size,
            "importance": loss.importance,
        }
    )
````
Capture the losses in the html page
````
{{ losses_data|json_script:"data" }}
````
    
