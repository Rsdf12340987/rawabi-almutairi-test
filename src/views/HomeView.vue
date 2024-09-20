<template>
  <div class="d-flex">
    <nav class="d-flex flex-column p-3 bg-light" style="width: 280px; height: 100vh;">
      <a href="#" class="d-flex align-items-center mb-3 mb-md-0 me-md-auto text-decoration-none">
        <img src="@/assets/lo1.svg" alt="logo" class="me-3 n" />
      </a>
      <hr />
      <ul class="nav nav-pills flex-column mb-auto">
        <li class="nav-item flex-grow-1">
          <a href="#" class="nav-link link-dark d-flex align-items-center">
            <img src="@/assets/home.svg" alt="Home" class="me-3 n" />
          </a>
        </li>
        <li class="nav-item flex-grow-1">
          <a href="#" class="nav-link link-dark d-flex align-items-center">
            <img src="@/assets/or.svg" alt="Orders" class="me-3 n" /> Orders
          </a>
        </li>
        <li class="nav-item flex-grow-1">
          <a href="#" class="nav-link link-dark d-flex align-items-center">
            <img src="@/assets/rev.svg" alt="Reviews" class="me-3 n" /> Reviews
          </a>
        </li>
        <li class="nav-item flex-grow-1">
          <a href="#" class="nav-link link-dark d-flex align-items-center">
            <img src="@/assets/cli.svg" alt="Clients" class="me-3 n" /> Clients
          </a>
        </li>
        <li class="nav-item flex-grow-1">
          <a href="#" class="nav-link link-dark d-flex align-items-center">
            <img src="@/assets/com.svg" alt="Companies" class="me-3 n" /> Companies
          </a>
        </li>
        <li class="nav-item flex-grow-1">
          <a href="#" class="nav-link link-dark d-flex align-items-center">
            <img src="@/assets/tru.svg" alt="Trucks" class="me-3 n" /> Trucks
          </a>
        </li>
        <li class="nav-item flex-grow-1">
          <a href="#" class="nav-link link-dark d-flex align-items-center">
            <img src="@/assets/ban.svg" alt="Brands" class="me-3 n" /> Brands
          </a>
        </li>
        <li class="nav-item flex-grow-1">
          <a href="#" class="nav-link link-dark d-flex align-items-center">
            <img src="@/assets/cities.svg" alt="Cities" class="me-3 n" /> Cities
          </a>
        </li>
        <li class="nav-item flex-grow-1">
          <a href="#" class="nav-link link-dark d-flex align-items-center">
            <img src="@/assets/contectman.svg" alt="Content Management" class="me-3 n" /> Content Management
          </a>
        </li>
        <li class="nav-item flex-grow-1">
          <a href="#" class="nav-link link-dark d-flex align-items-center">
            <img src="@/assets/per.svg" alt="Profile" class="me-3 n" />
          </a>
        </li>
        <li class="nav-item flex-grow-1">
          <a href="#" class="nav-link link-dark d-flex align-items-center">
            <img src="@/assets/sys.svg" alt="System Management" class="me-3 n" /> System Management
          </a>
        </li>
        <li class="nav-item flex-grow-1">
          <a href="#" class="nav-link link-dark d-flex align-items-center">
            <img src="@/assets/tran.svg" alt="Translation" class="me-3 n" /> Translation
          </a>
        </li>
        <li class="nav-item flex-grow-1">
          <a href="#" class="nav-link link-dark d-flex align-items-center">
            <img src="@/assets/cont.svg" alt="Contact" class="me-3 n" /> Contact
          </a>
        </li>
        <li class="nav-item flex-grow-1">
          <a href="#" class="nav-link link-dark d-flex align-items-center">
            <img src="@/assets/clint.svg" alt="Client Review" class="me-3 n" /> Client Review
          </a>
        </li>
      </ul>
    </nav>

    <main class="col-md-9 ms-sm-auto col-lg-10 px-4">
      <div class="d-flex justify-content-between align-items-center pt-3 pb-2 mb-3">
        <div class="d-flex flex-column align-items-start me-3">
        <h1 class="h2 mb-0">Dashboard Overview</h1>
        <p class="text-muted mb-0" style="font-size: 14px;">{{ formattedDate }}</p>
      </div>
      <div class="btn-toolbar d-flex align-items-center">
        <div class="btn-group me-2 d-flex align-items-center">
          <img src="@/assets/run.svg" alt="Run" class="me-2 n" />
          <img src="@/assets/line.svg" alt="Line" class="me-2 n" />
          <img src="@/assets/lo2.svg" alt="Logo" class="n" />
          <a class="nav-link dropdown-toggle" href="#" data-bs-toggle="dropdown" aria-expanded="false">
            INGOUDE COMPANY
          </a>
          <ul class="dropdown-menu">
            <li><a class="dropdown-item" href="#">1</a></li>
            <li><a class="dropdown-item" href="#">2</a></li>
          </ul>
        </div>
      </div>
    </div>
    <div class="d-flex align-items-center mb-4" style="gap: 10px;">
  <div class="form-check form-check-inline">
    <input class="form-check-input" type="radio" id="all" name="filter" value="all" checked />
    <label class="form-check-label" for="all">All</label>
  </div>
  <div class="form-check form-check-inline">
    <input class="form-check-input" type="radio" id="date" name="filter" value="date" />
    <label class="form-check-label" for="date"></label>
  </div>

  <div class="input-group" style="width: 140px;">
    <span class="input-group-text" style="font-size: 12px;">From</span>
    <input class="form-control" type="date" v-model="fromDate" aria-label="From date" style="font-size: 12px; height: 30px;" />
  </div>

  <div class="input-group" style="width: 140px;">
    <span class="input-group-text" style="font-size: 12px;">To</span>
    <input class="form-control" type="date" v-model="toDate" aria-label="To date" style="font-size: 12px; height: 30px;" />
  </div>

  <button class="btn btn-warning" @click="find" style="font-size: 12px;">Find</button>
</div>


      <div class="row mb-4 d-flex" style="gap: 10px; justify-content: flex-start;">
        <div class="col-auto p-0">
          <div class="card text-start" style="width: 270px; height: 120px; border-radius: 5px; border: 1px solid #ccc;">
            <div class="card-body">
              <h5 class="card-title text-dark" style="font-size: 12px; display: flex; align-items: center;">
                <img src="@/assets/ordersnum.svg" alt="Order Number" class="me-1" />Order Number
              </h5>
              <p class="card-text" style="font-size: 28px; opacity: 0.7;">1000 <sub style="font-size: 10px;">Orders</sub></p>
            </div>
          </div>
        </div>

        <div class="col-auto p-0">
          <div class="card text-start" style="width: 270px; height: 120px; border-radius: 5px; border: 1px solid #ccc;">
            <div class="card-body">
              <h5 class="card-title text-dark" style="font-size: 16px; display: flex; align-items: center;">
                <img src="@/assets/company.svg" alt="Company Number" class="me-1" />Company Number
              </h5>
              <p class="card-text" style="font-size: 28px; opacity: 0.7;">1000000 <sub style="font-size: 10px;">Orders</sub></p>
            </div>
          </div>
        </div>

        <div class="col-auto p-0">
          <div class="card text-start" style="width: 270px; height: 120px; border-radius: 5px; border: 1px solid #ccc;">
            <div class="card-body">
              <h5 class="card-title text-dark" style="font-size: 16px; display: flex; align-items: center;">
                <img src="@/assets/driv.svg" alt="Drivers Number" class="me-1" />Drivers Number
              </h5>
              <p class="card-text" style="font-size: 28px; opacity: 0.7;">500 <sub style="font-size: 10px;">Drivers</sub></p>
            </div>
          </div>
        </div>

        <div class="col-auto p-0">
          <div class="card text-start" style="width: 270px; height: 120px; border-radius: 5px; border: 1px solid #ccc;">
            <div class="card-body">
              <h5 class="card-title text-dark" style="font-size: 16px; display: flex; align-items: center;">
                <img src="@/assets/tota.svg" alt="Total Sales" class="me-1" />Total Sales
              </h5>
              <p class="card-text" style="font-size: 28px; opacity: 0.7;">500 <sub style="font-size: 10px;">SR</sub></p>
            </div>
          </div>
        </div>
      </div>

      <div class="d-flex flex-nowrap mb-4" style="gap: 10px; overflow-x: auto;">
        <div class="card" style="width: 270px; height: 220px; border-radius: 5px; border: 1px solid #dee2e6;">
          <div class="card-body text-center">
            <h5 class="card-title" style="font-size: 20px;">Waiting For Loading</h5>
            <div class="d-flex justify-content-center align-items-center">
              <div class="position-relative">
                <img src="@/assets/wit.svg" alt="Waiting for Loading" class="me-3 img-spacing" style="width: 135px; height: 135px;" />
              </div>
            </div>
          </div>
        </div>

        <div class="card" style="width: 270px; height: 220px; border-radius: 5px; border: 1px solid #dee2e6;">
          <div class="card-body text-center">
            <h5 class="card-title" style="font-size: 20px;">Waiting For Arrival</h5>
            <div class="d-flex justify-content-center align-items-center">
              <div class="position-relative">
                <img src="@/assets/ariiv.svg" alt="Waiting for Arrival" class="me-3 img-spacing" style="width: 135px; height: 135px;" />
              </div>
            </div>
          </div>
        </div>

        <div class="card" style="width: 270px; height: 220px; border-radius: 5px; border: 1px solid #dee2e6;">
          <div class="card-body text-center">
            <h5 class="card-title" style="font-size: 20px;">Completed</h5>
            <div class="d-flex justify-content-center align-items-center">
              <div class="position-relative">
                <img src="@/assets/rrr.svg" alt="Completed" class="me-3 img-spacing" style="width: 135px; height: 135px;" />
              </div>
            </div>
          </div>
        </div>

        <div class="card" style="width: 270px; height: 220px; border-radius: 5px; border: 1px solid #dee2e6;">
          <div class="card-body text-center">
            <h5 class="card-title" style="font-size: 20px;">Canceled</h5>
            <div class="d-flex justify-content-center align-items-center">
              <div class="position-relative">
                <img src="@/assets/canceld.svg" alt="Canceled" class="me-3 img-spacing" style="width: 135px; height: 135px;" />
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="d-flex flex-wrap mb-4" style="gap: 10px; overflow-x: auto;">
        <div class="card" style="width: 564px; height: 220px; border-radius: 5px; border: 1px solid #dee2e6;">
          <div class="card-body" style="padding: 15px;">
            <h5 class="card-title text-start" style="color:#353535; margin-bottom: 10px;">TOP 5 Companies</h5>
            <table class="table table-borderless mt-1" style="border: none;">
              <thead>
                <tr>
                  <th class="card-title text-start" style="color:#7E7E7E;">Company Name</th>
                  <th class="card-title text-start" style="color:#7E7E7E;">Order Qty</th>
                  <th class="card-title text-start" style="color:#7E7E7E;">Amount</th>
                </tr>
              </thead>
              <tbody>
                <tr>
                  <td style="text-align: left;">Gillette</td>
                  <td style="text-align: left;">5000</td>
                  <td style="text-align: left;">50000 SR</td>
                </tr>
                <tr>
                  <td style="text-align: left;">Louis Vuitton</td>
                  <td style="text-align: left;">3000</td>
                  <td style="text-align: left;">50000 SR</td>
                </tr>
                <tr>
                  <td style="text-align: left;">Johnson & Johnson</td>
                  <td style="text-align: left;">2000</td>
                  <td style="text-align: left;">50000 SR</td>
                </tr>
                <tr>
                  <td style="text-align: left;">Nintendo</td>
                  <td style="text-align: left;">1000</td>
                  <td style="text-align: left;">50000 SR</td>
                </tr>
              </tbody>
            </table>
          </div>
        </div>

        <div class="card" style="width: 270px; height: 220px; border-radius: 5px; border: 1px solid #dee2e6;">
          <div class="card-body text-center">
            <h5 class="card-title" style="font-size: 22px;">Order Repeated</h5>
            <div class="d-flex justify-content-center align-items-center">
              <div class="position-relative">
                <img src="@/assets/repat.svg" alt="Order Repeated" style="width: 135px; height: 135px; opacity: 1;" />
              </div>
            </div>
          </div>
        </div>

        <div class="card" style="width: 270px; height: 220px; border-radius: 5px; border: 1px solid #dee2e6;">
          <div class="card-body text-center">
            <h5 class="card-title" style="font-size: 22px;">Commission</h5>
            <div class="d-flex justify-content-center align-items-center">
              <div class="position-relative">
                <img src="@/assets/commi.svg" alt="Commission" style="width: 135px; height: 135px; opacity: 1;" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>

<script>
export default {
  data() {
    return {
      fromDate: '2023-09-26',
      toDate: '2023-09-26',
    };
  },
  computed: {
    formattedDate() {
      const options = { day: 'numeric', month: 'long', year: 'numeric' };
      return new Date().toLocaleDateString('en-US', options);
    }
  },
  methods: {
    find() {
      console.log(`Searching from ${this.fromDate} to ${this.toDate}`);
    }
  }
};


</script>

<style scoped>
.button {
  background-color: #FBA81A; /* لون الزر */
}
.form-check-input:checked {
  accent-color: #FBA81A; /* لون برتقالي */
}
</style>
