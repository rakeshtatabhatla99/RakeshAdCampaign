# RakeshAdCampaign
this is Ad Campaign project. It support 3 services:

1. createad : this is a post request where we need to provide the json 'Ad' object in below format to add the Ad in campaign
    
    URL : http://localhost:8080/MyAdCampaign/ad/AdCampaignService/createad
    METHOD : POST
    type : Application/json
    JSON AD Object:

    {
      "partner_id" : "Rakesh123",
       "duration" : 20,
       "ad_content" : "my bike add"
    }
    
    NOTE : duration is seconds which makes the ad live for specific duration in second
    It throw Exception if the Ad with same partner_id present and the duration is not expired
    
2. getAD : This can be used to search a Ad by providing partner_id
  
    http://localhost:8080/MyAdCampaign/ad/AdCampaignService/Rakesh123
    here 'Rakesh123' in URI is parther_id
    NOTE : It throws exception with message explaining if Ad not found with partner_id or if found but expired, else it will retunr 'Ad' json object

3. get all Ads
      http://localhost:8080/MyAdCampaign/ad/AdCampaignService/Rakesh123
      - this returns all the Ads in the list, it will include live and expired all the Ads
    
