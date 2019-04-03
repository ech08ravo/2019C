# Demo for an increasingly complex model 
From Maani & Cavana, Chapter 3

### A simple loop

![Alt text](https://g.gravizo.com/svg?
digraph Productivity_loop {
	label="Simple does it";
    Incoming_claims -> Pending_claims [label="s", weight=5];
    Incoming_claims -> Claim_settlement [label="s"];
    Claim_settlement -> Pending_claims [label="o"];
  }
)

### The productivity loop

![Alt text](https://g.gravizo.com/svg?
digraph Productivity_loop {
	label="Productivity Loop";
    Incoming_claims -> Pending_claims [label="s", weight=5];
    Incoming_claims -> Required_settlement_rate [label="s"]; 
    Claim_settlement -> Pending_claims [label="o", weight=10];
    Pending_claims -> Required_settlement_rate [label="s"];
    Required_settlement_rate -> Time_pressure [label="s"];
    Time_pressure -> Time_per_claim [label="o"];
    Time_per_claim -> Productivity [label="o", weight=5];
    Productivity -> Claim_settlement [label="s", weight=5];
  }
)

### Work week loop and burnout loop

Extending by two loops:

![Alt text](https://g.gravizo.com/svg?
digraph Productivity_loop {
	label="Two more loops";
    Incoming_claims -> Pending_claims [label="s", weight=5];
    Incoming_claims -> Required_settlement_rate [label="s"]; 
    Claim_settlement -> Pending_claims [label="o", weight=10];
    Pending_claims -> Required_settlement_rate [label="s"];
    Required_settlement_rate -> Time_pressure [label="s"];
    Time_pressure -> Time_per_claim [label="o"];
    Time_per_claim -> Productivity [label="o", weight=5];
    Productivity -> Claim_settlement [label="s", weight=5];
    subgraph Work_loop { 
		node[fontcolor="blue"];
    	Time_pressure -> Work_intensity [label="s"];
    	Work_intensity -> Productivity [label="s"];
  		}
  	subgraph Burnout_loop { 
		label="Burnout loop (B)";
		node[fontcolor="red"];
    	Work_intensity -> Burnout [label="s"];
    	Burnout -> Productivity [label="o"];
  		}
  }
)

### Adding the turnover loop

![Alt text](https://g.gravizo.com/svg?
digraph Productivity_loop {
	label="Maani Carvana Chapter 3";
	node[fontsize="14"];
    Incoming_claims -> Pending_claims [label="s", weight=5];
    Incoming_claims -> Required_settlement_rate [label="s"]; 
    Claim_settlement -> Pending_claims [label="o", weight=10];
    Pending_claims -> Required_settlement_rate [label="s"];
    Required_settlement_rate -> Time_pressure [label="s"];
    Time_pressure -> Time_per_claim [label="o"];
    Time_per_claim -> Productivity [label="o", weight=5];
    Productivity -> Claim_settlement [label="s", weight=5];
    subgraph "Work_loop" { 
		node[fontcolor="green"];
    	Time_pressure -> Work_intensity [label="s"];
    	Work_intensity -> Productivity [label="s"];
  		}
  	subgraph "Burnout loop" { 
		node[fontcolor="blue"];
    	Work_intensity -> Burnout [label="s"];
    	Burnout -> Productivity [label="o"];
    	  	subgraph "turnover loop" { 
		node[fontcolor="red"];
    	Time_available -> Time_pressure [label="o"];
    	Burnout -> Staff_turnover [label="s"];
    	Staff_turnover -> Assessors [label="o"];
    	Assessors -> Time_available [label="s"];
  		}
  	}
)

---end---