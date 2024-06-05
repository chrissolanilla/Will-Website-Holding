<div class="TeamContainer">
    <div class="TeamTitle">
        <h1>Team</h1>
    </div>
    <div class="TeamBios">
        <div class="Anthony statChild">
            <div class="Bio">
                <h3>Anthony J. Burke</h3>
                <p>
                    Anthony J. Burke, the Chief Executive Officer and founding 
                    partner of Burke Construction Group since 1997, brings over 
                    three decades of construction industry experience to his 
                    role. Beginning his career as a field engineer, Mr. Burke 
                    later founded The Tower Group, which he led for twelve years 
                    before its acquisition by an international firm, overseeing 
                    substantial growth to over 250 employees and $185 million in 
                    annual revenues. Prior to Tower, he served as President of 
                    the Construction Division for a prominent Florida developer, 
                    contributing to the construction of over 4.2 million square 
                    feet of commercial space.
                </p>
                <p>
                    A graduate of Indiana State University with a B.S. in Construction 
                    Management, Mr. Burke is also a State Certified General Contractor 
                    and has served on the State of Florida's Construction Industry 
                    Licensing Board, appointed by Governor Jeb Bush. He currently 
                    provides advisory support to his church board alongside his 
                    leadership responsibilities at Burke Construction Group.
                </p>
            </div>
            <div class="AnthonyImg">
                <img
                    src="Anthony-J.-Burke-2018.jpg"
                    alt="Chief Executive Officer, Anthony J Burke"
                />
            </div>
        </div>

        <div class="David statChild">
            <div class="BioReverse">
                <h3>David Martinez</h3>
                <p>
                    David W. Martinez is a seasoned financial professional 
                    with over twenty-eight years of experience in accounting, 
                    financial management, and the construction industry. 
                    Beginning his career as a staff accountant and local 
                    municipality auditor, he swiftly ascended to senior 
                    management positions, culminating in the establishment 
                    of his own CPA firm.
                </p>
                <p>
                    As Chief Financial Officer and Partner at The Tower Group, Inc., 
                    and co-founder of Burke Construction Group, Inc., David has overseen 
                    multimillion-dollar projects and demonstrated a keen understanding 
                    of financial markets. With credentials including a Bachelor of 
                    Accounting from Florida International University and certifications 
                    as a Certified Public Accountant, he brings a wealth of expertise to 
                    his role as a qualified investor in private equity.
                </p>
            </div>
            <div class="DavidImg">
                <img
                    src="David-W-M.jpg"
                    alt="Chief Financial Officer, David Martinez"
                />
            </div>
        </div>

        <div class="Steve statChild">
            <div class="Bio">
                <h3>Steve Alessi</h3>
                <p>
                    Pastor Steve Alessi, a native of Miami, has dedicated over 
                    four decades to ministry, answering his calling with 
                    unwavering devotion. Since graduating from Southeastern 
                    University in 1984, he has served diligently, initially as 
                    Associate Pastor of Grace Church of Kendall alongside his 
                    parents. In 1997, he and his wife, Mary, founded Metro Life 
                    Church in Doral, Florida, and later assumed leadership of 
                    Grace Church, transforming it into the Dadeland Campus of 
                    Metro Life Church.
                </p>
                <p>
                    Today, Pastor Steve leads Metro Life Church with his family, 
                    overseeing its local and online campuses, while also 
                    inspiring men through Goodfellas Camps and sharing his 
                    powerful journey of resilience following a near-fatal heart 
                    attack in 2007, which he chronicled in his book, "Forty Two - 
                    How To Finish Strong When You Thought You Were Finished." 
                    Beyond ministry, he actively engages with his community, 
                    serving on advisory boards and as a chaplain. Pastor Steve 
                    finds joy in hunting, boating, and traveling with loved ones, 
                    epitomizing a life dedicated to faith, family, and service.
                </p>
            </div>
            <div class="SteveImg">
                <img src="Steve.jpg" alt="Temp Title, Steve Alessi" />
            </div>
        </div>
    </div>
</div>

<style>
    .TeamContainer {
        color: white;
        width: 100%;
        max-width: 100rem;
        height: auto;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 4px;
        padding: 1rem;
    }

    .TeamTitle {
        margin-bottom: 2rem;
    }

    .TeamBios {
        width: 100%;
        max-width: 100rem;
        height: auto;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 50px;
    }

    .Anthony,
    .David,
    .Steve {
        border-radius: 1rem;
        padding: 1rem;
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 4px;
        flex-direction: row-reverse;
    }

    .Anthony {
        background: linear-gradient(
            89.2deg,
            rgb(48, 170, 163) 5.3%,
            rgb(5, 120, 190) 94.7%
        );
    }

    .David {
        background: linear-gradient(
            -225deg,
            #3d4e81 0%,
            #5753c9 48%,
            #6e7ff3 100%
        );
    }

    .Steve {
        background: linear-gradient(to right, #243949 0%, #517fa4 100%);
    }

    .Bio,
    .BioReverse {
        width: 100%;
        font-size: 20px;
        display: block;
        position: relative;
        padding: 0 20px;
    }

    .Bio h3,
    .BioReverse h3 {
        margin-top: 0;
    }

    .AnthonyImg img,
    .DavidImg img,
    .SteveImg img {
        border-radius: 1rem;
        width: 100%;
        height: auto;
    }

    @media (max-width: 900px) {
        .TeamBios {
            gap: 20px;
        }

        .Anthony,
        .David,
        .Steve {
            flex-direction: column-reverse;
            text-align: center;
            padding: 1rem;
        }

        .Bio,
        .BioReverse {
            padding: 0;
        }

        .AnthonyImg,
        .DavidImg,
        .SteveImg {
            max-width: 100%;
            margin-bottom: 1rem;
        }

        .Bio p,
        .BioReverse p {
            font-size: 1rem;
            margin-bottom: 10px;
        }
    }
</style>
