## Serverless and Mashup: Money is not Everything
_Serverless Track_

_Wojciech Gawroński, Pattern Match_

Pattern Match has 7 project that runs totally serverless. 
Operational glue - they used lambda for many things to manage all services together. 


Many papers treat on how serverless will change the dev environment. 
Many things we know now will be invalidated by serverless. For example persistent connection to DB, how we preserve this while scaling? We can see that often companies are "compute first" because it is much more easier that "storage first" because managing state is much more harder.


#### Traits of serverless architecture:
Trait is neutral, be aware of that and embrace it. In some context it could be a positive or negative characteristic.
[The traits of serverless architecture](https://www.thoughtworks.com/insights/blog/traits-serverless-architecture):
- Low barrier to entry
- Hostless - that's dumb explanation of serverless
- Stateless - this helps scale, in fact without state you can scale infinitely
- Elasticity
- Distributed

The security should always be your concern. There are always new vectors of attacks. There was a hole in AWS lambda (?)

Serverless 1.0 landscape has many parts that are not mature [The Cloud Native Interactive Landscape](https://github.com/cncf/landscape).

#### Real cost (TCO)
Many think that serverless will be more expensive. But this depends on context. One must know the costs of infrastructure and employment because both could be reduced or raised by serverless. As always, Peopleware, Software, Hardware is a cost.

All cloud providers are pushing on delivering market value. Serverless reduce time to market.  

#### Trade-offs of serverless
- state - managing state is very hard (ex. storage)
- infant landscape - above
- vendor lock - many do not know that services like IAM or serving VR are more likely to be vendor-lock than databases or lambdas.

Embrace the traits. Context is the king. Serverless 2.0 is coming.

#### QA
**How can you block buring budget on AWS?** Monitoring, alerts etc. Create button to kill all infrastructure when leaving the office.

**What do you think about serverless framework?** Many clients are asking if this will make them cloud-independent. But that's not yet the case. Maybe in feature. 

**With limited time (1 month) what would you choose lambda vs kube?** I would go with lambda. 
